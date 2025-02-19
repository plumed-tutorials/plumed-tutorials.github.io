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
[fv-az1690-151:06285] *** Process received signal ***
[fv-az1690-151:06285] Signal: Aborted (6)
[fv-az1690-151:06285] Signal code:  (-6)
[fv-az1690-151:06285] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb52c645330]
[fv-az1690-151:06285] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb52c69eb2c]
[fv-az1690-151:06285] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb52c64527e]
[fv-az1690-151:06285] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb52c6288ff]
[fv-az1690-151:06285] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb52caa5ff5]
[fv-az1690-151:06285] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb52cabb0da]
[fv-az1690-151:06285] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb52caa5a55]
[fv-az1690-151:06285] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb52caa5a6f]
[fv-az1690-151:06285] [ 8] plumed(+0x13209)[0x55d0e2782209]
[fv-az1690-151:06285] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb52c62a1ca]
[fv-az1690-151:06285] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb52c62a28b]
[fv-az1690-151:06285] [11] plumed(+0x134a5)[0x55d0e27824a5]
[fv-az1690-151:06285] *** End of error message ***
</pre>
{% endraw %}
