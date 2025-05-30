Stderr for source:  examples.md_working_3.dat   
Download: [zipped raw stdout](examples.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](examples.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action LOAD with label @0 : cannot understand the following words from the input line : GLOBAL
[pkrvmf6wy0o8zjz:58997] *** Process received signal ***
[pkrvmf6wy0o8zjz:58997] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58997] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58997] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb6bf045330]
[pkrvmf6wy0o8zjz:58997] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb6bf09eb2c]
[pkrvmf6wy0o8zjz:58997] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb6bf04527e]
[pkrvmf6wy0o8zjz:58997] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb6bf0288ff]
[pkrvmf6wy0o8zjz:58997] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb6bf4a5ff5]
[pkrvmf6wy0o8zjz:58997] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb6bf4bb0da]
[pkrvmf6wy0o8zjz:58997] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb6bf4a5a55]
[pkrvmf6wy0o8zjz:58997] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb6bf4a5a6f]
[pkrvmf6wy0o8zjz:58997] [ 8] plumed(+0x13209)[0x558a69ea3209]
[pkrvmf6wy0o8zjz:58997] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb6bf02a1ca]
[pkrvmf6wy0o8zjz:58997] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb6bf02a28b]
[pkrvmf6wy0o8zjz:58997] [11] plumed(+0x134a5)[0x558a69ea34a5]
[pkrvmf6wy0o8zjz:58997] *** End of error message ***
</pre>
{% endraw %}
