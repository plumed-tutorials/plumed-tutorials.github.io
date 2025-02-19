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
[fv-az1755-505:07703] *** Process received signal ***
[fv-az1755-505:07703] Signal: Aborted (6)
[fv-az1755-505:07703] Signal code:  (-6)
[fv-az1755-505:07703] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1e80445330]
[fv-az1755-505:07703] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1e8049eb2c]
[fv-az1755-505:07703] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1e8044527e]
[fv-az1755-505:07703] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1e804288ff]
[fv-az1755-505:07703] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1e808a5ff5]
[fv-az1755-505:07703] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1e808bb0da]
[fv-az1755-505:07703] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1e808a5a55]
[fv-az1755-505:07703] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1e808a5a6f]
[fv-az1755-505:07703] [ 8] plumed(+0x13209)[0x55a4229ae209]
[fv-az1755-505:07703] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1e8042a1ca]
[fv-az1755-505:07703] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1e8042a28b]
[fv-az1755-505:07703] [11] plumed(+0x134a5)[0x55a4229ae4a5]
[fv-az1755-505:07703] *** End of error message ***
</pre>
{% endraw %}
