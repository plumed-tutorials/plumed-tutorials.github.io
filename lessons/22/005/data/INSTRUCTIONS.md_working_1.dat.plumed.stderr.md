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
[fv-az1429-301:04638] *** Process received signal ***
[fv-az1429-301:04638] Signal: Aborted (6)
[fv-az1429-301:04638] Signal code:  (-6)
[fv-az1429-301:04638] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f8026c42520]
[fv-az1429-301:04638] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f8026c969fc]
[fv-az1429-301:04638] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f8026c42476]
[fv-az1429-301:04638] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f8026c287f3]
[fv-az1429-301:04638] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f80270a2b9e]
[fv-az1429-301:04638] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f80270ae20c]
[fv-az1429-301:04638] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f80270ae277]
[fv-az1429-301:04638] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f80270ae52b]
[fv-az1429-301:04638] [ 8] plumed(+0x12f48)[0x56060ed71f48]
[fv-az1429-301:04638] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f8026c29d90]
[fv-az1429-301:04638] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f8026c29e40]
[fv-az1429-301:04638] [11] plumed(+0x131e5)[0x56060ed721e5]
[fv-az1429-301:04638] *** End of error message ***
</pre>
{% endraw %}
