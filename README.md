I need WebGL2-compute for my new game. It is "supported" by chrome in theory, but in reality i've ran into a problem:

$ chromium-browser --enable-webgl2-compute-context --use-cmd-decoder=passthrough --use-angle=gl
^[[A[29280:29280:1018/173515.247259:ERROR:gles2_cmd_decoder.cc(3545)] ContextResult::kFatalFailure: webgl2-compute is not supported on validating command decoder.
$ chromium-browser --enable-webgl2-compute-context --use-angle=gl --use-passthrough-cmd-decoder
[29964:29964:1018/173650.067521:ERROR:gles2_cmd_decoder.cc(3545)] ContextResult::kFatalFailure: webgl2-compute is not supported on validating command decoder.

This shit doesn't work, and anyway, I don't want clients to use unsafe options to run my game.
Fixing chromium is a pain in ass because their coding style is totally incompatible with me, and there must be a simplier way to do this.
Thats why I've decided to implement command decoder as a separate library.
