Stderr for source:  examples.md_working_2.dat   
Download: [zipped raw stdout](examples.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](examples.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action LOAD with label @0 : cannot understand the following words from the input line : GLOBAL
[pkrvmf6wy0o8zjz:58993] *** Process received signal ***
[pkrvmf6wy0o8zjz:58993] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58993] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58993] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f03b3645330]
[pkrvmf6wy0o8zjz:58993] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f03b369eb2c]
[pkrvmf6wy0o8zjz:58993] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f03b364527e]
[pkrvmf6wy0o8zjz:58993] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f03b36288ff]
[pkrvmf6wy0o8zjz:58993] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f03b3aa5ff5]
[pkrvmf6wy0o8zjz:58993] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f03b3abb0da]
[pkrvmf6wy0o8zjz:58993] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f03b3aa5a55]
[pkrvmf6wy0o8zjz:58993] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f03b3aa5a6f]
[pkrvmf6wy0o8zjz:58993] [ 8] plumed(+0x13209)[0x55f30198f209]
[pkrvmf6wy0o8zjz:58993] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f03b362a1ca]
[pkrvmf6wy0o8zjz:58993] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f03b362a28b]
[pkrvmf6wy0o8zjz:58993] [11] plumed(+0x134a5)[0x55f30198f4a5]
[pkrvmf6wy0o8zjz:58993] *** End of error message ***
</pre>
{% endraw %}
