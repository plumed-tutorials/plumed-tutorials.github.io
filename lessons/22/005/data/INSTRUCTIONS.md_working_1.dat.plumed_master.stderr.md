Stderr for source:  INSTRUCTIONS.md_working_1.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(pytorch/PytorchModel.cpp:135) PLMD::function::pytorch::PytorchModel::PytorchModel(const PLMD::ActionOptions&)
The FILE: 'torch_model.ptc' does not exist.
[fv-az1279-640:06383] *** Process received signal ***
[fv-az1279-640:06383] Signal: Aborted (6)
[fv-az1279-640:06383] Signal code:  (-6)
[fv-az1279-640:06383] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fad0bc45330]
[fv-az1279-640:06383] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fad0bc9eb2c]
[fv-az1279-640:06383] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fad0bc4527e]
[fv-az1279-640:06383] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fad0bc288ff]
[fv-az1279-640:06383] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fad0c0a5ff5]
[fv-az1279-640:06383] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fad0c0bb0da]
[fv-az1279-640:06383] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fad0c0a5a55]
[fv-az1279-640:06383] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fad0c0a5a6f]
[fv-az1279-640:06383] [ 8] plumed_master(+0x146dd)[0x55b69533b6dd]
[fv-az1279-640:06383] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fad0bc2a1ca]
[fv-az1279-640:06383] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fad0bc2a28b]
[fv-az1279-640:06383] [11] plumed_master(+0x15365)[0x55b69533c365]
[fv-az1279-640:06383] *** End of error message ***
</pre>
{% endraw %}
