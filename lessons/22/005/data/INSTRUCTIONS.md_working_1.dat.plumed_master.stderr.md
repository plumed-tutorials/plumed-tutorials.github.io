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
[fv-az1429-301:04646] *** Process received signal ***
[fv-az1429-301:04646] Signal: Aborted (6)
[fv-az1429-301:04646] Signal code:  (-6)
[fv-az1429-301:04646] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f70dee42520]
[fv-az1429-301:04646] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f70dee969fc]
[fv-az1429-301:04646] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f70dee42476]
[fv-az1429-301:04646] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f70dee287f3]
[fv-az1429-301:04646] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f70df2a2b9e]
[fv-az1429-301:04646] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f70df2ae20c]
[fv-az1429-301:04646] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f70df2ae277]
[fv-az1429-301:04646] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f70df2ae52b]
[fv-az1429-301:04646] [ 8] plumed_master(+0x14254)[0x5623102ee254]
[fv-az1429-301:04646] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f70dee29d90]
[fv-az1429-301:04646] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f70dee29e40]
[fv-az1429-301:04646] [11] plumed_master(+0x14eb5)[0x5623102eeeb5]
[fv-az1429-301:04646] *** End of error message ***
</pre>
{% endraw %}