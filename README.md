## Project Description
This is a forked repository. The original OpenCV repository is [here](https://github.com/opencv/opencv.git).

## The PR I'm Currently Working On

[[#19259] Minimal implementation of GpuMatND](https://github.com/opencv/opencv/pull/19259) ([test code in contrib](https://github.com/opencv/opencv_contrib/pull/2805))

## List of Merged PRs ([opencv](https://github.com/opencv/opencv/pulls?utf8=%E2%9C%93&q=author%3Anglee))

[[#18136] bit-exact cuda::equalizeHist](https://github.com/opencv/opencv/pull/18136)  
[[#17982] cuda::GpuMat::convertTo - fix for in-place arguments](https://github.com/opencv/opencv/pull/17982)  
[[#17863] cuda::flip - Use in-place npp function for inplace arguments](https://github.com/opencv/opencv/pull/17863) ([port to contrib](https://github.com/opencv/opencv_contrib/pull/2612))  
[[#17556] cuda optflow TVL1 : run safely in async mode](https://github.com/opencv/opencv/pull/17556)  
[[#14041] Extract Ptr-related code from lut.cu to new lut.cpp](https://github.com/opencv/opencv/pull/14041)  
[[#14000] CUDA 10.1 Build Issue Fix on Master Branch](https://github.com/opencv/opencv/pull/14000)  
[[#13960] Windows Build Issue Fix](https://github.com/opencv/opencv/pull/13960)  
_(20)_  
[[#13958] CUDA 10.1 Build Issue Fix](https://github.com/opencv/opencv/pull/13958)  
[[#13903] cudev - Rework some code](https://github.com/opencv/opencv/pull/13903)  
[[#13850] cuda::StereoBM - Fix hanging and racing issue](https://github.com/opencv/opencv/pull/13850)  
[[#13810] cudalegacy: Use safe block scan function](https://github.com/opencv/opencv/pull/13810)  
[[#13764] Add CV_16UC1 support for cuda::CLAHE](https://github.com/opencv/opencv/pull/13764)  
[[#13658] `__shfl_up_sync` with mask for CUDA >= 9](https://github.com/opencv/opencv/pull/13658)  
[[#13625] Fix Farneback Optical Flow Algorithm](https://github.com/opencv/opencv/pull/13625)  
[[#13596] Remove build warning msg with CUDA 10.0](https://github.com/opencv/opencv/pull/13596)  
[[#13364] Fix error in LineIterator example code in doc](https://github.com/opencv/opencv/pull/13364)  
[[#11572] NPP : NppStreamHandler fix](https://github.com/opencv/opencv/pull/11572)  
_(10)_  
[[#11526] cuda_meanStdDev : bug fix](https://github.com/opencv/opencv/pull/11526)  
[[#11483] cuda_canny : multi stream safety](https://github.com/opencv/opencv/pull/11483)  
[[#11155] Update GpuMat, GpuMat::download, GpuMat::upload documentation](https://github.com/opencv/opencv/pull/11155)  
[[#11110] test_buffer_pool: synchronize after async copy](https://github.com/opencv/opencv/pull/11110)  
[[#10987] SSE2 : use `_mm_cvtpd_epi32` when converting from CV_64F to CV_32S](https://github.com/opencv/opencv/pull/10987)  
[[#10906] cuda_fast : multi stream safety](https://github.com/opencv/opencv/pull/10906)  
[[#10861] Fix for CUDA_Arithm/Dft.Algorithm/0 test](https://github.com/opencv/opencv/pull/10861)  
[[#10803] Update BufferReader documentation with some example code](https://github.com/opencv/opencv/pull/10803)  
[[#10751] cuda_stream: do not allocate GPU memory by default](https://github.com/opencv/opencv/pull/10751)  
[[#10640] cv::cuda::cvtColor bug fix](https://github.com/opencv/opencv/pull/10640)  

## List of Involved PRs ([opencv](https://github.com/opencv/opencv/pulls?q=is%3Apr+involves%3Anglee+-author%3Anglee))

[[#19286] (move semantics)add cuda::Stream constructor from cudaStream_t](https://github.com/opencv/opencv/pull/19286#discussion_r561625069)  
[[#17432] CUDA: choose supported CC automatically](https://github.com/opencv/opencv/pull/17432)  
[[#12722] cudafilters: fix test failure of cudafilters Median_Accuracy](https://github.com/opencv/opencv/pull/12722)  
[[#11064] cudaarithm: make the asynchronous call to NPP safe](https://github.com/opencv/opencv/pull/11064)

## List of Involved Discussions ([opencv](https://github.com/opencv/opencv/issues?utf8=%E2%9C%93&q=involves:nglee+is:issue), [opencv_contrib](https://github.com/opencv/opencv_contrib/issues?utf8=%E2%9C%93&q=involves:nglee+is:issue))

[[#18347] cudaarithm: inplace version of NPP flip fails with odd number ROI](https://github.com/opencv/opencv/issues/18347)  
_(30)_  
[[#18155] cuda_OpticalFlowDual_TVL1 is not thread-safe in python](https://github.com/opencv/opencv/issues/18155)  
[[#18051] CUDA GoodFeaturesToTrackDetector is not ThreadSafe ?](https://github.com/opencv/opencv/issues/18051)  
[[#18035] CUDA equalizeHist does not produce identical result](https://github.com/opencv/opencv/issues/18035)  
[[#17840] In-place flip of GpuMat produces image artifacs](https://github.com/opencv/opencv/issues/17840)  
[[#13092] cv::cuda::GpuMat.convertTo() seems not to support in-place, while cv::Mat does](https://github.com/opencv/opencv/issues/13092)  
[[#16013] Corrupted optical flow using cuda::DenseOpticalFlow asynchronously in multithreaded environment](https://github.com/opencv/opencv/issues/16013)  
[[#2361] (contrib)Bug in cv::cuda::warpPerspective](https://github.com/opencv/opencv_contrib/issues/2361)  
[[#14052] an illegal memory access was encountered in function 'download'](https://github.com/opencv/opencv/issues/14052)  
[[#14017] Opencv 4.0.1 with Cuda](https://github.com/opencv/opencv/issues/14017)  
[[#13996] opencv-4.0.1 ,CUDA10.1, failed to build cudaimageproc](https://github.com/opencv/opencv/issues/13996)  
_(20)_  
[[#13984] Problem compiling clahe.cu - identifier "PtrStepus" is undefined](https://github.com/opencv/opencv/issues/13984)  
[[#13952] OpenCV 4.0.1 + Cuda 10.1, failed to build?](https://github.com/opencv/opencv/issues/13952)  
[[#13897] Failed to build OpenCV 4.0.1 with CUDA 10 10.0](https://github.com/opencv/opencv/issues/13897)  
[[#13883] Template Matching is not threadsafe](https://github.com/opencv/opencv/issues/13883)  
[[#13761] cudalegacy NCVHaarObjectDetection hangs with RTX 2080 Ti](https://github.com/opencv/opencv/issues/13761)  
[[#13491] Error when building with CUDA. VS 2017, Win10.](https://github.com/opencv/opencv/issues/13491)  
[[#1958] (contrib)Feature request: Cuda CLAHE for 16 bit images](https://github.com/opencv/opencv_contrib/issues/1958)  
[[#13477] cuda::createTemplateMatching not work with CUDA10.0](https://github.com/opencv/opencv/issues/13477)  
[[#13014] cuda blockScanInclusive hangs with RTX 2080](https://github.com/opencv/opencv/issues/13014)  
[[#12895] cudaoptflow: test failure of FarnebackOpticalFlow](https://github.com/opencv/opencv/issues/12895)  
_(10)_  
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

## Waiting for Response - For my own reference :)
[[#11606] Suggestion for the CUDA stream module](https://github.com/opencv/opencv/issues/11606)  
[[#12585] cuda: move CUDA modules to opencv_contrib](https://github.com/opencv/opencv/pull/12585)  
