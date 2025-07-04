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
[pkrvmbietmlfzoi:35683] *** Process received signal ***
[pkrvmbietmlfzoi:35683] Signal: Aborted (6)
[pkrvmbietmlfzoi:35683] Signal code:  (-6)
[pkrvmbietmlfzoi:35683] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb638245330]
[pkrvmbietmlfzoi:35683] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb63829eb2c]
[pkrvmbietmlfzoi:35683] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb63824527e]
[pkrvmbietmlfzoi:35683] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb6382288ff]
[pkrvmbietmlfzoi:35683] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb6386a5ff5]
[pkrvmbietmlfzoi:35683] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb6386bb0da]
[pkrvmbietmlfzoi:35683] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb6386a5a55]
[pkrvmbietmlfzoi:35683] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb6386a5a6f]
[pkrvmbietmlfzoi:35683] [ 8] plumed(+0x13209)[0x559aba713209]
[pkrvmbietmlfzoi:35683] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb63822a1ca]
[pkrvmbietmlfzoi:35683] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb63822a28b]
[pkrvmbietmlfzoi:35683] [11] plumed(+0x134a5)[0x559aba7134a5]
[pkrvmbietmlfzoi:35683] *** End of error message ***
</pre>
{% endraw %}
