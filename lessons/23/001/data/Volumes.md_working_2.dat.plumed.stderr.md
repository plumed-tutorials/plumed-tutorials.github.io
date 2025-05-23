Stderr for source:  Volumes.md_working_2.dat   
Download: [zipped raw stdout](Volumes.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Volumes.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action INSPHERE with label sp : keyword DATA is compulsory for this action
[pkrvmf6wy0o8zjz:60329] *** Process received signal ***
[pkrvmf6wy0o8zjz:60329] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60329] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60329] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f8ad5445330]
[pkrvmf6wy0o8zjz:60329] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f8ad549eb2c]
[pkrvmf6wy0o8zjz:60329] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f8ad544527e]
[pkrvmf6wy0o8zjz:60329] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f8ad54288ff]
[pkrvmf6wy0o8zjz:60329] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f8ad58a5ff5]
[pkrvmf6wy0o8zjz:60329] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f8ad58bb0da]
[pkrvmf6wy0o8zjz:60329] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f8ad58a5a55]
[pkrvmf6wy0o8zjz:60329] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f8ad58a5a6f]
[pkrvmf6wy0o8zjz:60329] [ 8] plumed(+0x13209)[0x55a4a791e209]
[pkrvmf6wy0o8zjz:60329] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f8ad542a1ca]
[pkrvmf6wy0o8zjz:60329] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f8ad542a28b]
[pkrvmf6wy0o8zjz:60329] [11] plumed(+0x134a5)[0x55a4a791e4a5]
[pkrvmf6wy0o8zjz:60329] *** End of error message ***
</pre>
{% endraw %}
