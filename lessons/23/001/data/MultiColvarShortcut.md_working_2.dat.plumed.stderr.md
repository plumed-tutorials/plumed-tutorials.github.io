Stderr for source:  MultiColvarShortcut.md_working_2.dat   
Download: [zipped raw stdout](MultiColvarShortcut.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvarShortcut.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[fv-az1755-505:05533] *** Process received signal ***
[fv-az1755-505:05533] Signal: Aborted (6)
[fv-az1755-505:05533] Signal code:  (-6)
[fv-az1755-505:05533] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f518c245330]
[fv-az1755-505:05533] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f518c29eb2c]
[fv-az1755-505:05533] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f518c24527e]
[fv-az1755-505:05533] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f518c2288ff]
[fv-az1755-505:05533] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f518c6a5ff5]
[fv-az1755-505:05533] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f518c6bb0da]
[fv-az1755-505:05533] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f518c6a5a55]
[fv-az1755-505:05533] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f518c6a5a6f]
[fv-az1755-505:05533] [ 8] plumed(+0x13209)[0x55a75cf15209]
[fv-az1755-505:05533] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f518c22a1ca]
[fv-az1755-505:05533] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f518c22a28b]
[fv-az1755-505:05533] [11] plumed(+0x134a5)[0x55a75cf154a5]
[fv-az1755-505:05533] *** End of error message ***
</pre>
{% endraw %}
