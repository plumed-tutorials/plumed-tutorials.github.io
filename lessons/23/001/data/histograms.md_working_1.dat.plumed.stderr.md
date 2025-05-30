Stderr for source:  histograms.md_working_1.dat   
Download: [zipped raw stdout](histograms.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @2 : keyword GRID is compulsory for this action
[pkrvmf6wy0o8zjz:61071] *** Process received signal ***
[pkrvmf6wy0o8zjz:61071] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61071] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61071] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ffaea445330]
[pkrvmf6wy0o8zjz:61071] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ffaea49eb2c]
[pkrvmf6wy0o8zjz:61071] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ffaea44527e]
[pkrvmf6wy0o8zjz:61071] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ffaea4288ff]
[pkrvmf6wy0o8zjz:61071] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ffaea8a5ff5]
[pkrvmf6wy0o8zjz:61071] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ffaea8bb0da]
[pkrvmf6wy0o8zjz:61071] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ffaea8a5a55]
[pkrvmf6wy0o8zjz:61071] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ffaea8a5a6f]
[pkrvmf6wy0o8zjz:61071] [ 8] plumed(+0x13209)[0x55ffb48e1209]
[pkrvmf6wy0o8zjz:61071] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ffaea42a1ca]
[pkrvmf6wy0o8zjz:61071] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ffaea42a28b]
[pkrvmf6wy0o8zjz:61071] [11] plumed(+0x134a5)[0x55ffb48e14a5]
[pkrvmf6wy0o8zjz:61071] *** End of error message ***
</pre>
{% endraw %}
