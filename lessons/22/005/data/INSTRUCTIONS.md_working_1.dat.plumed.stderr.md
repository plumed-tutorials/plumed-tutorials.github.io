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
[fv-az1279-640:06367] *** Process received signal ***
[fv-az1279-640:06367] Signal: Aborted (6)
[fv-az1279-640:06367] Signal code:  (-6)
[fv-az1279-640:06367] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9b4fc45330]
[fv-az1279-640:06367] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9b4fc9eb2c]
[fv-az1279-640:06367] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9b4fc4527e]
[fv-az1279-640:06367] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9b4fc288ff]
[fv-az1279-640:06367] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9b500a5ff5]
[fv-az1279-640:06367] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9b500bb0da]
[fv-az1279-640:06367] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9b500a5a55]
[fv-az1279-640:06367] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9b500a5a6f]
[fv-az1279-640:06367] [ 8] plumed(+0x13209)[0x563c1bb08209]
[fv-az1279-640:06367] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9b4fc2a1ca]
[fv-az1279-640:06367] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9b4fc2a28b]
[fv-az1279-640:06367] [11] plumed(+0x134a5)[0x563c1bb084a5]
[fv-az1279-640:06367] *** End of error message ***
</pre>
{% endraw %}
