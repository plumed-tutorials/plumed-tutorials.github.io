Stderr for source:  Behler.md_working_5.dat   
Download: [zipped raw stdout](Behler.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Behler.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1755-505:07031] *** Process received signal ***
[fv-az1755-505:07031] Signal: Aborted (6)
[fv-az1755-505:07031] Signal code:  (-6)
[fv-az1755-505:07031] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7feee5445330]
[fv-az1755-505:07031] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7feee549eb2c]
[fv-az1755-505:07031] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7feee544527e]
[fv-az1755-505:07031] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7feee54288ff]
[fv-az1755-505:07031] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7feee58a5ff5]
[fv-az1755-505:07031] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7feee58bb0da]
[fv-az1755-505:07031] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7feee58a5a55]
[fv-az1755-505:07031] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7feee58a5a6f]
[fv-az1755-505:07031] [ 8] plumed(+0x13209)[0x560303730209]
[fv-az1755-505:07031] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7feee542a1ca]
[fv-az1755-505:07031] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7feee542a28b]
[fv-az1755-505:07031] [11] plumed(+0x134a5)[0x5603037304a5]
[fv-az1755-505:07031] *** End of error message ***
</pre>
{% endraw %}
