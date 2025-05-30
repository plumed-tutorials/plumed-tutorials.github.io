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
[pkrvmf6wy0o8zjz:60189] *** Process received signal ***
[pkrvmf6wy0o8zjz:60189] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60189] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60189] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f62ca845330]
[pkrvmf6wy0o8zjz:60189] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f62ca89eb2c]
[pkrvmf6wy0o8zjz:60189] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f62ca84527e]
[pkrvmf6wy0o8zjz:60189] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f62ca8288ff]
[pkrvmf6wy0o8zjz:60189] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f62caca5ff5]
[pkrvmf6wy0o8zjz:60189] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f62cacbb0da]
[pkrvmf6wy0o8zjz:60189] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f62caca5a55]
[pkrvmf6wy0o8zjz:60189] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f62caca5a6f]
[pkrvmf6wy0o8zjz:60189] [ 8] plumed(+0x13209)[0x55ff29990209]
[pkrvmf6wy0o8zjz:60189] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f62ca82a1ca]
[pkrvmf6wy0o8zjz:60189] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f62ca82a28b]
[pkrvmf6wy0o8zjz:60189] [11] plumed(+0x134a5)[0x55ff299904a5]
[pkrvmf6wy0o8zjz:60189] *** End of error message ***
</pre>
{% endraw %}
