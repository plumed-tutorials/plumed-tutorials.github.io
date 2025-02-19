Stderr for source:  Steinhardt.md_working_10.dat   
Download: [zipped raw stdout](Steinhardt.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action PRINT with label @2 : action lq6 has no component named lq6 (hint! the components in this actions are: )
[fv-az1755-505:06484] *** Process received signal ***
[fv-az1755-505:06484] Signal: Aborted (6)
[fv-az1755-505:06484] Signal code:  (-6)
[fv-az1755-505:06484] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa649a45330]
[fv-az1755-505:06484] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa649a9eb2c]
[fv-az1755-505:06484] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa649a4527e]
[fv-az1755-505:06484] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa649a288ff]
[fv-az1755-505:06484] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa649ea5ff5]
[fv-az1755-505:06484] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa649ebb0da]
[fv-az1755-505:06484] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa649ea5a55]
[fv-az1755-505:06484] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa649ea5a6f]
[fv-az1755-505:06484] [ 8] plumed(+0x13209)[0x55c7443bd209]
[fv-az1755-505:06484] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa649a2a1ca]
[fv-az1755-505:06484] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa649a2a28b]
[fv-az1755-505:06484] [11] plumed(+0x134a5)[0x55c7443bd4a5]
[fv-az1755-505:06484] *** End of error message ***
</pre>
{% endraw %}
