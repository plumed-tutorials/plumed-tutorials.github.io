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
[pkrvmbietmlfzoi:35699] *** Process received signal ***
[pkrvmbietmlfzoi:35699] Signal: Aborted (6)
[pkrvmbietmlfzoi:35699] Signal code:  (-6)
[pkrvmbietmlfzoi:35699] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f84c7c45330]
[pkrvmbietmlfzoi:35699] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f84c7c9eb2c]
[pkrvmbietmlfzoi:35699] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f84c7c4527e]
[pkrvmbietmlfzoi:35699] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f84c7c288ff]
[pkrvmbietmlfzoi:35699] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f84c80a5ff5]
[pkrvmbietmlfzoi:35699] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f84c80bb0da]
[pkrvmbietmlfzoi:35699] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f84c80a5a55]
[pkrvmbietmlfzoi:35699] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f84c80a5a6f]
[pkrvmbietmlfzoi:35699] [ 8] plumed_master(+0x146dd)[0x558bd43f66dd]
[pkrvmbietmlfzoi:35699] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f84c7c2a1ca]
[pkrvmbietmlfzoi:35699] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f84c7c2a28b]
[pkrvmbietmlfzoi:35699] [11] plumed_master(+0x15365)[0x558bd43f7365]
[pkrvmbietmlfzoi:35699] *** End of error message ***
</pre>
{% endraw %}
