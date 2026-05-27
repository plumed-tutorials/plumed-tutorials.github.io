Stderr for source:  INSTRUCTIONS.md_working_1.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(pytorch/PytorchModel.cpp:138) PLMD::function::pytorch::PytorchModel::PytorchModel(const PLMD::ActionOptions&)
The FILE: 'torch_model.ptc' does not exist.
[runnervm3jyl0:80184] *** Process received signal ***
[runnervm3jyl0:80184] Signal: Aborted (6)
[runnervm3jyl0:80184] Signal code:  (-6)
[runnervm3jyl0:80184] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe0b7e45330]
[runnervm3jyl0:80184] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe0b7e9eb2c]
[runnervm3jyl0:80184] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe0b7e4527e]
[runnervm3jyl0:80184] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe0b7e288ff]
[runnervm3jyl0:80184] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe0b82a5ff5]
[runnervm3jyl0:80184] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe0b82bb0da]
[runnervm3jyl0:80184] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe0b82a5a55]
[runnervm3jyl0:80184] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe0b82a5a6f]
[runnervm3jyl0:80184] [ 8] plumed_master(+0x146dd)[0x5622634c56dd]
[runnervm3jyl0:80184] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe0b7e2a1ca]
[runnervm3jyl0:80184] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe0b7e2a28b]
[runnervm3jyl0:80184] [11] plumed_master(+0x15365)[0x5622634c6365]
[runnervm3jyl0:80184] *** End of error message ***
</pre>
{% endraw %}
