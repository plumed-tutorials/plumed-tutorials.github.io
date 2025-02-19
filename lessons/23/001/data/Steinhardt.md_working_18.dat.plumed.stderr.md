Stderr for source:  Steinhardt.md_working_18.dat   
Download: [zipped raw stdout](Steinhardt.md_working_18.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_18.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1755-505:06748] *** Process received signal ***
[fv-az1755-505:06748] Signal: Aborted (6)
[fv-az1755-505:06748] Signal code:  (-6)
[fv-az1755-505:06748] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5680845330]
[fv-az1755-505:06748] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f568089eb2c]
[fv-az1755-505:06748] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f568084527e]
[fv-az1755-505:06748] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f56808288ff]
[fv-az1755-505:06748] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f5680ca5ff5]
[fv-az1755-505:06748] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f5680cbb0da]
[fv-az1755-505:06748] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f5680ca5a55]
[fv-az1755-505:06748] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f5680ca5a6f]
[fv-az1755-505:06748] [ 8] plumed(+0x13209)[0x55dfb0bb6209]
[fv-az1755-505:06748] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f568082a1ca]
[fv-az1755-505:06748] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f568082a28b]
[fv-az1755-505:06748] [11] plumed(+0x134a5)[0x55dfb0bb64a5]
[fv-az1755-505:06748] *** End of error message ***
</pre>
{% endraw %}
