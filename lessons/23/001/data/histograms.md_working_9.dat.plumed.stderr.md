Stderr for source:  histograms.md_working_9.dat   
Download: [zipped raw stdout](histograms.md_working_9.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_9.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCES with label d1 : keyword ATOMS could not be read correctly
[pkrvmf6wy0o8zjz:61341] *** Process received signal ***
[pkrvmf6wy0o8zjz:61341] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61341] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61341] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2b66045330]
[pkrvmf6wy0o8zjz:61341] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f2b6609eb2c]
[pkrvmf6wy0o8zjz:61341] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f2b6604527e]
[pkrvmf6wy0o8zjz:61341] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f2b660288ff]
[pkrvmf6wy0o8zjz:61341] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2b664a5ff5]
[pkrvmf6wy0o8zjz:61341] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2b664bb0da]
[pkrvmf6wy0o8zjz:61341] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2b664a5a55]
[pkrvmf6wy0o8zjz:61341] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2b664a5a6f]
[pkrvmf6wy0o8zjz:61341] [ 8] plumed(+0x13209)[0x561c3aec4209]
[pkrvmf6wy0o8zjz:61341] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f2b6602a1ca]
[pkrvmf6wy0o8zjz:61341] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f2b6602a28b]
[pkrvmf6wy0o8zjz:61341] [11] plumed(+0x134a5)[0x561c3aec44a5]
[pkrvmf6wy0o8zjz:61341] *** End of error message ***
</pre>
{% endraw %}
