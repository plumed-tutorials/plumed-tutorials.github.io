Stderr for source:  INSTRUCTIONS.md_working_1.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(pytorch/PytorchModel.cpp:124) PLMD::function::pytorch::PytorchModel::PytorchModel(const PLMD::ActionOptions&)
The FILE: 'torch_model.ptc' does not exist.
[fv-az665-16:70326] *** Process received signal ***
[fv-az665-16:70326] Signal: Aborted (6)
[fv-az665-16:70326] Signal code:  (-6)
[fv-az665-16:70326] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f8c53042520]
[fv-az665-16:70326] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f8c530969fc]
[fv-az665-16:70326] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f8c53042476]
[fv-az665-16:70326] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f8c530287f3]
[fv-az665-16:70326] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f8c534a2b9e]
[fv-az665-16:70326] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f8c534ae20c]
[fv-az665-16:70326] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f8c534ae277]
[fv-az665-16:70326] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f8c534ae52b]
[fv-az665-16:70326] [ 8] plumed(+0x12f48)[0x55f0003e9f48]
[fv-az665-16:70326] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f8c53029d90]
[fv-az665-16:70326] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f8c53029e40]
[fv-az665-16:70326] [11] plumed(+0x131e5)[0x55f0003ea1e5]
[fv-az665-16:70326] *** End of error message ***
</pre>
{% endraw %}
