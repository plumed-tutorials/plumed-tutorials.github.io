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
[pkrvmf6wy0o8zjz:60125] *** Process received signal ***
[pkrvmf6wy0o8zjz:60125] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60125] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60125] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3a0f245330]
[pkrvmf6wy0o8zjz:60125] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3a0f29eb2c]
[pkrvmf6wy0o8zjz:60125] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3a0f24527e]
[pkrvmf6wy0o8zjz:60125] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3a0f2288ff]
[pkrvmf6wy0o8zjz:60125] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f3a0f6a5ff5]
[pkrvmf6wy0o8zjz:60125] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f3a0f6bb0da]
[pkrvmf6wy0o8zjz:60125] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f3a0f6a5a55]
[pkrvmf6wy0o8zjz:60125] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f3a0f6a5a6f]
[pkrvmf6wy0o8zjz:60125] [ 8] plumed(+0x13209)[0x55c2d4431209]
[pkrvmf6wy0o8zjz:60125] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3a0f22a1ca]
[pkrvmf6wy0o8zjz:60125] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3a0f22a28b]
[pkrvmf6wy0o8zjz:60125] [11] plumed(+0x134a5)[0x55c2d44314a5]
[pkrvmf6wy0o8zjz:60125] *** End of error message ***
</pre>
{% endraw %}
