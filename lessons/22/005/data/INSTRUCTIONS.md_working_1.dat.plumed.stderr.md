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
[fv-az573-691:04989] *** Process received signal ***
[fv-az573-691:04989] Signal: Aborted (6)
[fv-az573-691:04989] Signal code:  (-6)
[fv-az573-691:04989] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fe1abe42520]
[fv-az573-691:04989] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fe1abe969fc]
[fv-az573-691:04989] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fe1abe42476]
[fv-az573-691:04989] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fe1abe287f3]
[fv-az573-691:04989] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fe1ac2a2b9e]
[fv-az573-691:04989] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fe1ac2ae20c]
[fv-az573-691:04989] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fe1ac2ae277]
[fv-az573-691:04989] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fe1ac2ae52b]
[fv-az573-691:04989] [ 8] plumed(+0x12f48)[0x5600b8c5af48]
[fv-az573-691:04989] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fe1abe29d90]
[fv-az573-691:04989] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fe1abe29e40]
[fv-az573-691:04989] [11] plumed(+0x131e5)[0x5600b8c5b1e5]
[fv-az573-691:04989] *** End of error message ***
</pre>
{% endraw %}
