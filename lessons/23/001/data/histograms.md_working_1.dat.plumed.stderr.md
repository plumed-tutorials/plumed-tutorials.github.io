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
[pkrvmf6wy0o8zjz:60821] *** Process received signal ***
[pkrvmf6wy0o8zjz:60821] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60821] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60821] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2ce9245330]
[pkrvmf6wy0o8zjz:60821] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f2ce929eb2c]
[pkrvmf6wy0o8zjz:60821] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f2ce924527e]
[pkrvmf6wy0o8zjz:60821] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f2ce92288ff]
[pkrvmf6wy0o8zjz:60821] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2ce96a5ff5]
[pkrvmf6wy0o8zjz:60821] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2ce96bb0da]
[pkrvmf6wy0o8zjz:60821] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2ce96a5a55]
[pkrvmf6wy0o8zjz:60821] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2ce96a5a6f]
[pkrvmf6wy0o8zjz:60821] [ 8] plumed(+0x13209)[0x55bbceebb209]
[pkrvmf6wy0o8zjz:60821] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f2ce922a1ca]
[pkrvmf6wy0o8zjz:60821] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f2ce922a28b]
[pkrvmf6wy0o8zjz:60821] [11] plumed(+0x134a5)[0x55bbceebb4a5]
[pkrvmf6wy0o8zjz:60821] *** End of error message ***
</pre>
{% endraw %}
