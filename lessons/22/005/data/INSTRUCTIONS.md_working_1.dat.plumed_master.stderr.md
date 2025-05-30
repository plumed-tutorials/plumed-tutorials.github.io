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
[pkrvmf6wy0o8zjz:60205] *** Process received signal ***
[pkrvmf6wy0o8zjz:60205] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60205] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60205] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f94bea45330]
[pkrvmf6wy0o8zjz:60205] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f94bea9eb2c]
[pkrvmf6wy0o8zjz:60205] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f94bea4527e]
[pkrvmf6wy0o8zjz:60205] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f94bea288ff]
[pkrvmf6wy0o8zjz:60205] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f94beea5ff5]
[pkrvmf6wy0o8zjz:60205] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f94beebb0da]
[pkrvmf6wy0o8zjz:60205] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f94beea5a55]
[pkrvmf6wy0o8zjz:60205] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f94beea5a6f]
[pkrvmf6wy0o8zjz:60205] [ 8] plumed_master(+0x146dd)[0x561bdbc1c6dd]
[pkrvmf6wy0o8zjz:60205] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f94bea2a1ca]
[pkrvmf6wy0o8zjz:60205] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f94bea2a28b]
[pkrvmf6wy0o8zjz:60205] [11] plumed_master(+0x15365)[0x561bdbc1d365]
[pkrvmf6wy0o8zjz:60205] *** End of error message ***
</pre>
{% endraw %}
