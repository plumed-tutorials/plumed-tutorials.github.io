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
[pkrvmf6wy0o8zjz:60141] *** Process received signal ***
[pkrvmf6wy0o8zjz:60141] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60141] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60141] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f465f245330]
[pkrvmf6wy0o8zjz:60141] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f465f29eb2c]
[pkrvmf6wy0o8zjz:60141] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f465f24527e]
[pkrvmf6wy0o8zjz:60141] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f465f2288ff]
[pkrvmf6wy0o8zjz:60141] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f465f6a5ff5]
[pkrvmf6wy0o8zjz:60141] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f465f6bb0da]
[pkrvmf6wy0o8zjz:60141] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f465f6a5a55]
[pkrvmf6wy0o8zjz:60141] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f465f6a5a6f]
[pkrvmf6wy0o8zjz:60141] [ 8] plumed_master(+0x146dd)[0x555aa782e6dd]
[pkrvmf6wy0o8zjz:60141] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f465f22a1ca]
[pkrvmf6wy0o8zjz:60141] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f465f22a28b]
[pkrvmf6wy0o8zjz:60141] [11] plumed_master(+0x15365)[0x555aa782f365]
[pkrvmf6wy0o8zjz:60141] *** End of error message ***
</pre>
{% endraw %}
