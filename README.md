# OpenCV Contributions — Namgoo Lee

Contributed **32 merged** upstream pull requests to OpenCV's CUDA stack — **29** in [opencv](https://github.com/opencv/opencv/pulls?utf8=%E2%9C%93&q=author%3Anglee) and **3** in [opencv_contrib](https://github.com/opencv/opencv_contrib/pulls?q=author%3Anglee)

## Key impact areas

- **Designed and implemented GpuMatND** — an N-dimensional GPU matrix type for CUDA. ([#19259](https://github.com/opencv/opencv/pull/19259), interoperability test code in contrib [#2805](https://github.com/opencv/opencv_contrib/pull/2805))
- **Eliminated multi-stream race conditions** across the CUDA module — data races and hangs in FAST, Canny, StereoBM, and TVL1 optical flow. ([#10906](https://github.com/opencv/opencv/pull/10906), [#11483](https://github.com/opencv/opencv/pull/11483), [#13850](https://github.com/opencv/opencv/pull/13850), [#17556](https://github.com/opencv/opencv/pull/17556))
- **Achieved bit-exact GPU/CPU parity** for histogram equalization. ([#18136](https://github.com/opencv/opencv/pull/18136))
- **Improved CUDA toolkit compatibility** across multiple releases (CUDA 9–10.1), keeping the build green. ([#14000](https://github.com/opencv/opencv/pull/14000), [#13958](https://github.com/opencv/opencv/pull/13958), [#13658](https://github.com/opencv/opencv/pull/13658), [#13596](https://github.com/opencv/opencv/pull/13596))
- **Added in-place NPP paths** for `cuda::flip` and `GpuMat::convertTo`, avoiding extra GPU buffers. ([#17863](https://github.com/opencv/opencv/pull/17863), ported to contrib [#2612](https://github.com/opencv/opencv_contrib/pull/2612); [#17982](https://github.com/opencv/opencv/pull/17982))

## Merged PRs by theme

### GPU data structures & memory
- [[#19259] Minimal implementation of GpuMatND](https://github.com/opencv/opencv/pull/19259) (test code in contrib [#2805](https://github.com/opencv/opencv_contrib/pull/2805))
- [[#17982] cuda::GpuMat::convertTo — fix for in-place arguments](https://github.com/opencv/opencv/pull/17982)
- [[#10751] cuda_stream: do not allocate GPU memory by default](https://github.com/opencv/opencv/pull/10751)

### Thread / multi-stream safety
- [[#17556] cuda optflow TVL1: run safely in async mode](https://github.com/opencv/opencv/pull/17556)
- [[#13850] cuda::StereoBM — fix hanging and racing issue](https://github.com/opencv/opencv/pull/13850)
- [[#13810] cudalegacy: use safe block scan function](https://github.com/opencv/opencv/pull/13810)
- [[#11572] NPP: NppStreamHandler fix](https://github.com/opencv/opencv/pull/11572)
- [[#11483] cuda_canny: multi stream safety](https://github.com/opencv/opencv/pull/11483)
- [[#11110] test_buffer_pool: synchronize after async copy](https://github.com/opencv/opencv/pull/11110)
- [[#10906] cuda_fast: multi stream safety](https://github.com/opencv/opencv/pull/10906)

### Numerical correctness & algorithm fixes
- [[#18136] bit-exact cuda::equalizeHist](https://github.com/opencv/opencv/pull/18136)
- [[#17863] cuda::flip — use in-place npp function for inplace arguments](https://github.com/opencv/opencv/pull/17863) (ported to contrib [#2612](https://github.com/opencv/opencv_contrib/pull/2612))
- [[#13764] Add CV_16UC1 support for cuda::CLAHE](https://github.com/opencv/opencv/pull/13764)
- [[#13625] Fix Farneback Optical Flow algorithm](https://github.com/opencv/opencv/pull/13625)
- [[#11526] cuda_meanStdDev: bug fix](https://github.com/opencv/opencv/pull/11526)
- [[#10987] SSE2: use `_mm_cvtpd_epi32` when converting from CV_64F to CV_32S](https://github.com/opencv/opencv/pull/10987)
- [[#10861] Fix for CUDA_Arithm/Dft.Algorithm/0 test](https://github.com/opencv/opencv/pull/10861)
- [[#10640] cv::cuda::cvtColor bug fix](https://github.com/opencv/opencv/pull/10640)

### Build, CI & toolchain compatibility
- [[#14000] CUDA 10.1 build issue fix on master branch](https://github.com/opencv/opencv/pull/14000)
- [[#13960] Windows build issue fix](https://github.com/opencv/opencv/pull/13960)
- [[#13958] CUDA 10.1 build issue fix](https://github.com/opencv/opencv/pull/13958)
- [[#13658] `__shfl_up_sync` with mask for CUDA >= 9](https://github.com/opencv/opencv/pull/13658)
- [[#13596] Remove build warning message with CUDA 10.0](https://github.com/opencv/opencv/pull/13596)

### Refactoring & code quality
- [[#22041] Remove const from functions returning by value](https://github.com/opencv/opencv/pull/22041) (contrib counterpart [#3266](https://github.com/opencv/opencv_contrib/pull/3266))
- [[#14041] Extract Ptr-related code from lut.cu to new lut.cpp](https://github.com/opencv/opencv/pull/14041)
- [[#13903] cudev — rework some code](https://github.com/opencv/opencv/pull/13903)

### Documentation
- [[#11155] Update GpuMat, GpuMat::download, GpuMat::upload documentation](https://github.com/opencv/opencv/pull/11155)
- [[#13364] Fix error in LineIterator example code in doc](https://github.com/opencv/opencv/pull/13364)
- [[#10803] Update BufferReader documentation with example code](https://github.com/opencv/opencv/pull/10803)

## Code Review & Design Discussion

Contributed via review, design discussion, and code to PRs authored by others — most of which merged:

- [[#16666] [WIP] Add GpuMatND with arbitrary dimension support](https://github.com/opencv/opencv/pull/16666) — earlier community design attempt; later delivered as my merged [#19259](https://github.com/opencv/opencv/pull/19259)
- [[#19534] cudafilters: remove dangerous race condition](https://github.com/opencv/opencv/pull/19534) — merged; CUDA filter thread-safety, my core area
- [[#13695] Fix cuda::filter corrupted output across threads/streams](https://github.com/opencv/opencv/pull/13695) — merged; multi-stream correctness in cudafilters
- [[#11064] cudaarithm: make the asynchronous call to NPP safe](https://github.com/opencv/opencv/pull/11064) — merged; aligns with my own NPP / stream-safety work ([#11572](https://github.com/opencv/opencv/pull/11572), [#11483](https://github.com/opencv/opencv/pull/11483), [#10906](https://github.com/opencv/opencv/pull/10906))

<details>
<summary>Full list of PRs I was involved in but did not author (for reference) — <a href="https://github.com/opencv/opencv/pulls?q=is:pr+involves:nglee+-author:nglee">opencv</a>, <a href="https://github.com/opencv/opencv_contrib/pulls?q=is:pr+involves:nglee+-author:nglee">opencv_contrib</a></summary>

[[#19534] cudafilters: remove dangerous race condition](https://github.com/opencv/opencv/pull/19534) (merged)  
[[#19286] add cuda::Stream constructor with cuda stream flags](https://github.com/opencv/opencv/pull/19286) (merged)  
[[#17671] CUDA: fix native detection on Jetson](https://github.com/opencv/opencv/pull/17671) (merged)  
[[#17581] CUDA: fix build error on Jetson TX1 and TX2](https://github.com/opencv/opencv/pull/17581) (merged)  
[[#17432] CUDA: choose supported CC automatically](https://github.com/opencv/opencv/pull/17432) (merged)  
[[#16666] [WIP] Add GpuMatND with arbitrary dimension support](https://github.com/opencv/opencv/pull/16666) (closed)  
[[#13695] Fix cuda::filter corrupted output across threads/streams](https://github.com/opencv/opencv/pull/13695) (merged)  
[[#12722] cudafilters: fix test failure of Median_Accuracy](https://github.com/opencv/opencv/pull/12722) (merged)  
[[#12585] cuda: move CUDA modules to opencv_contrib](https://github.com/opencv/opencv/pull/12585) (merged)  
[[#11951] cmake: allow to use external FindCUDA from modern CMake](https://github.com/opencv/opencv/pull/11951) (merged)  
[[#11064] cudaarithm: make the asynchronous call to NPP safe](https://github.com/opencv/opencv/pull/11064) (merged)  

</details>

## Issue investigation & design proposals

**Diagnosed community bug reports and shipped the merged fix:**

- [#18035](https://github.com/opencv/opencv/issues/18035) (non-deterministic CUDA equalizeHist) → fixed in [#18136](https://github.com/opencv/opencv/pull/18136)
- [#17840](https://github.com/opencv/opencv/issues/17840) (in-place GpuMat flip artifacts) → fixed in [#17863](https://github.com/opencv/opencv/pull/17863)
- [#13092](https://github.com/opencv/opencv/issues/13092) (GpuMat::convertTo in-place) → fixed in [#17982](https://github.com/opencv/opencv/pull/17982)
- [#16013](https://github.com/opencv/opencv/issues/16013) / [#18155](https://github.com/opencv/opencv/issues/18155) (TVL1 optical flow unsafe in async/multithreaded use) → fixed in [#17556](https://github.com/opencv/opencv/pull/17556)

**Reported and fixed myself:**

- [#8725](https://github.com/opencv/opencv/issues/8725) (stray `cudaMalloc()` from `Stream::Null()`) → fixed in [#10751](https://github.com/opencv/opencv/pull/10751)

**Design proposals / RFCs I opened:**

- [[#11606] Suggestion for the CUDA stream module](https://github.com/opencv/opencv/issues/11606)

<details>
<summary>Full list of issues I reported or was involved in (for reference) — <a href="https://github.com/opencv/opencv/issues?utf8=%E2%9C%93&q=involves:nglee+is:issue">opencv</a>, <a href="https://github.com/opencv/opencv_contrib/issues?utf8=%E2%9C%93&q=involves:nglee+is:issue">opencv_contrib</a></summary>

[[#24115] RFC cuda::Stream — documentation issue and usage inconsistency](https://github.com/opencv/opencv/issues/24115)  
[[#18347] cudaarithm: inplace version of NPP flip fails with odd number ROI](https://github.com/opencv/opencv/issues/18347)  
[[#18155] cuda_OpticalFlowDual_TVL1 is not thread-safe in python](https://github.com/opencv/opencv/issues/18155)  
[[#18051] CUDA GoodFeaturesToTrackDetector is not ThreadSafe ?](https://github.com/opencv/opencv/issues/18051)  
[[#18035] CUDA equalizeHist does not produce identical result](https://github.com/opencv/opencv/issues/18035)  
[[#17840] In-place flip of GpuMat produces image artifacs](https://github.com/opencv/opencv/issues/17840)  
[[#16433] GpuMat as input/output to cv::dnn::Net](https://github.com/opencv/opencv/issues/16433)  
[[#16013] Corrupted optical flow using cuda::DenseOpticalFlow asynchronously in multithreaded environment](https://github.com/opencv/opencv/issues/16013)  
[[#13092] cv::cuda::GpuMat.convertTo() seems not to support in-place, while cv::Mat does](https://github.com/opencv/opencv/issues/13092)  
[[#2724] (contrib) Error building with BUILD_CUDA_STUB on machine without CUDA](https://github.com/opencv/opencv_contrib/issues/2724)  
[[#2361] (contrib) Bug in cv::cuda::warpPerspective](https://github.com/opencv/opencv_contrib/issues/2361)  
[[#14052] an illegal memory access was encountered in function 'download'](https://github.com/opencv/opencv/issues/14052)  
[[#14017] Opencv 4.0.1 with Cuda](https://github.com/opencv/opencv/issues/14017)  
[[#13996] opencv-4.0.1, CUDA10.1, failed to build cudaimageproc](https://github.com/opencv/opencv/issues/13996)  
[[#13984] Problem compiling clahe.cu — identifier "PtrStepus" is undefined](https://github.com/opencv/opencv/issues/13984)  
[[#13952] OpenCV 4.0.1 + Cuda 10.1, failed to build?](https://github.com/opencv/opencv/issues/13952)  
[[#13897] Failed to build OpenCV 4.0.1 with CUDA 10 10.0](https://github.com/opencv/opencv/issues/13897)  
[[#13883] Template Matching is not threadsafe](https://github.com/opencv/opencv/issues/13883)  
[[#13761] cudalegacy NCVHaarObjectDetection hangs with RTX 2080 Ti](https://github.com/opencv/opencv/issues/13761)  
[[#13491] Error when building with CUDA. VS 2017, Win10.](https://github.com/opencv/opencv/issues/13491)  
[[#1958] (contrib) Feature request: Cuda CLAHE for 16 bit images](https://github.com/opencv/opencv_contrib/issues/1958)  
[[#13477] cuda::createTemplateMatching not work with CUDA10.0](https://github.com/opencv/opencv/issues/13477)  
[[#13014] cuda blockScanInclusive hangs with RTX 2080](https://github.com/opencv/opencv/issues/13014)  
[[#12895] cudaoptflow: test failure of FarnebackOpticalFlow](https://github.com/opencv/opencv/issues/12895)  
[[#12721] cudafilters: Median_Accuracy fails with CUDA 9.0 and after](https://github.com/opencv/opencv/issues/12721)  
[[#12320] cv::cuda::integral hangs on Titan V](https://github.com/opencv/opencv/issues/12320)  
[[#11622] CUDA Median filter tests fail with CUDA 9.1 but pass with CUDA 8.0](https://github.com/opencv/opencv/issues/11622)  
[[#11606] Suggestion for the CUDA stream module](https://github.com/opencv/opencv/issues/11606)  
[[#11511] unneeded cudaStreamSynchronize(stream_)](https://github.com/opencv/opencv/issues/11511)  
[[#11298] bug in MemoryReturn in cuda module](https://github.com/opencv/opencv/issues/11298)  
[[#11063] cudaarithm: async call to NPP fails](https://github.com/opencv/opencv/issues/11063)  
[[#8938] Can `–default-stream per-thread` be used with opencv ?](https://github.com/opencv/opencv/issues/8938)  
[[#8725] Calling cv::cuda::Stream::Null() results in a stray cudaMalloc() call](https://github.com/opencv/opencv/issues/8725)  
[[#6742] cv::cuda::Filter thread safety](https://github.com/opencv/opencv/issues/6742)  

</details>
