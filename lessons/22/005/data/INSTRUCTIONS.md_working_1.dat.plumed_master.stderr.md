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
[fv-az573-691:04997] *** Process received signal ***
[fv-az573-691:04997] Signal: Aborted (6)
[fv-az573-691:04997] Signal code:  (-6)
[fv-az573-691:04997] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fae1a842520]
[fv-az573-691:04997] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fae1a8969fc]
[fv-az573-691:04997] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fae1a842476]
[fv-az573-691:04997] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fae1a8287f3]
[fv-az573-691:04997] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fae1aca2b9e]
[fv-az573-691:04997] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fae1acae20c]
[fv-az573-691:04997] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fae1acae277]
[fv-az573-691:04997] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fae1acae52b]
[fv-az573-691:04997] [ 8] plumed_master(+0x14254)[0x558af1d36254]
[fv-az573-691:04997] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fae1a829d90]
[fv-az573-691:04997] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fae1a829e40]
[fv-az573-691:04997] [11] plumed_master(+0x14eb5)[0x558af1d36eb5]
[fv-az573-691:04997] *** End of error message ***
</pre>
{% endraw %}
