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
[runnervm3jyl0:80169] *** Process received signal ***
[runnervm3jyl0:80169] Signal: Aborted (6)
[runnervm3jyl0:80169] Signal code:  (-6)
[runnervm3jyl0:80169] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6ed6245330]
[runnervm3jyl0:80169] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6ed629eb2c]
[runnervm3jyl0:80169] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6ed624527e]
[runnervm3jyl0:80169] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6ed62288ff]
[runnervm3jyl0:80169] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6ed66a5ff5]
[runnervm3jyl0:80169] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6ed66bb0da]
[runnervm3jyl0:80169] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6ed66a5a55]
[runnervm3jyl0:80169] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6ed66a5a6f]
[runnervm3jyl0:80169] [ 8] plumed(+0x13209)[0x558defca0209]
[runnervm3jyl0:80169] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6ed622a1ca]
[runnervm3jyl0:80169] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6ed622a28b]
[runnervm3jyl0:80169] [11] plumed(+0x134a5)[0x558defca04a5]
[runnervm3jyl0:80169] *** End of error message ***
</pre>
{% endraw %}
