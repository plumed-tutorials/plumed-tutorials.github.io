Stderr for source:  INSTRUCTIONS.md_working_1.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(pytorch/PytorchModel.cpp:122) PLMD::function::pytorch::PytorchModel::PytorchModel(const PLMD::ActionOptions&)
The FILE: 'torch_model.ptc' does not exist.
[runnervm3jyl0:48215] *** Process received signal ***
[runnervm3jyl0:48215] Signal: Aborted (6)
[runnervm3jyl0:48215] Signal code:  (-6)
[runnervm3jyl0:48215] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ffbcfe45330]
[runnervm3jyl0:48215] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ffbcfe9eb2c]
[runnervm3jyl0:48215] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ffbcfe4527e]
[runnervm3jyl0:48215] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ffbcfe288ff]
[runnervm3jyl0:48215] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ffbd02a5ff5]
[runnervm3jyl0:48215] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ffbd02bb0da]
[runnervm3jyl0:48215] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ffbd02a5a55]
[runnervm3jyl0:48215] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ffbd02a5a6f]
[runnervm3jyl0:48215] [ 8] plumed(+0x13209)[0x55ff19619209]
[runnervm3jyl0:48215] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ffbcfe2a1ca]
[runnervm3jyl0:48215] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ffbcfe2a28b]
[runnervm3jyl0:48215] [11] plumed(+0x134a5)[0x55ff196194a5]
[runnervm3jyl0:48215] *** End of error message ***
</pre>
{% endraw %}
