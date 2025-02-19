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
[fv-az1755-505:07830] *** Process received signal ***
[fv-az1755-505:07830] Signal: Aborted (6)
[fv-az1755-505:07830] Signal code:  (-6)
[fv-az1755-505:07830] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fdbe3445330]
[fv-az1755-505:07830] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fdbe349eb2c]
[fv-az1755-505:07830] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fdbe344527e]
[fv-az1755-505:07830] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fdbe34288ff]
[fv-az1755-505:07830] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fdbe38a5ff5]
[fv-az1755-505:07830] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fdbe38bb0da]
[fv-az1755-505:07830] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fdbe38a5a55]
[fv-az1755-505:07830] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fdbe38a5a6f]
[fv-az1755-505:07830] [ 8] plumed(+0x13209)[0x55924adef209]
[fv-az1755-505:07830] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fdbe342a1ca]
[fv-az1755-505:07830] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fdbe342a28b]
[fv-az1755-505:07830] [11] plumed(+0x134a5)[0x55924adef4a5]
[fv-az1755-505:07830] *** End of error message ***
</pre>
{% endraw %}
