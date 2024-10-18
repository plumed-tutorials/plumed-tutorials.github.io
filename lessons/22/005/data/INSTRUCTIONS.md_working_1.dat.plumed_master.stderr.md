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
[fv-az665-16:70334] *** Process received signal ***
[fv-az665-16:70334] Signal: Aborted (6)
[fv-az665-16:70334] Signal code:  (-6)
[fv-az665-16:70334] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fd1cc642520]
[fv-az665-16:70334] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fd1cc6969fc]
[fv-az665-16:70334] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fd1cc642476]
[fv-az665-16:70334] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fd1cc6287f3]
[fv-az665-16:70334] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fd1ccaa2b9e]
[fv-az665-16:70334] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fd1ccaae20c]
[fv-az665-16:70334] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fd1ccaae277]
[fv-az665-16:70334] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fd1ccaae52b]
[fv-az665-16:70334] [ 8] plumed_master(+0x14254)[0x55ad41357254]
[fv-az665-16:70334] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fd1cc629d90]
[fv-az665-16:70334] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fd1cc629e40]
[fv-az665-16:70334] [11] plumed_master(+0x14eb5)[0x55ad41357eb5]
[fv-az665-16:70334] *** End of error message ***
</pre>
{% endraw %}
