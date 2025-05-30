Stderr for source:  histograms.md_working_5.dat   
Download: [zipped raw stdout](histograms.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[pkrvmf6wy0o8zjz:61196] *** Process received signal ***
[pkrvmf6wy0o8zjz:61196] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61196] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61196] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fdc8ba45330]
[pkrvmf6wy0o8zjz:61196] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fdc8ba9eb2c]
[pkrvmf6wy0o8zjz:61196] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fdc8ba4527e]
[pkrvmf6wy0o8zjz:61196] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fdc8ba288ff]
[pkrvmf6wy0o8zjz:61196] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fdc8bea5ff5]
[pkrvmf6wy0o8zjz:61196] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fdc8bebb0da]
[pkrvmf6wy0o8zjz:61196] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fdc8bea5a55]
[pkrvmf6wy0o8zjz:61196] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fdc8bea5a6f]
[pkrvmf6wy0o8zjz:61196] [ 8] plumed(+0x13209)[0x564aba958209]
[pkrvmf6wy0o8zjz:61196] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fdc8ba2a1ca]
[pkrvmf6wy0o8zjz:61196] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fdc8ba2a28b]
[pkrvmf6wy0o8zjz:61196] [11] plumed(+0x134a5)[0x564aba9584a5]
[pkrvmf6wy0o8zjz:61196] *** End of error message ***
</pre>
{% endraw %}
