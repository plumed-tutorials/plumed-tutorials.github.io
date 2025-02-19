Stderr for source:  ./solutions/walker-0/plumed_reweight.dat   
Download: [zipped raw stdout](plumed_reweight.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_reweight.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @33 : keyword ARG is compulsory for this action
[fv-az1755-505:05427] *** Process received signal ***
[fv-az1755-505:05427] Signal: Aborted (6)
[fv-az1755-505:05427] Signal code:  (-6)
[fv-az1755-505:05427] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fbca5045330]
[fv-az1755-505:05427] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fbca509eb2c]
[fv-az1755-505:05427] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fbca504527e]
[fv-az1755-505:05427] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fbca50288ff]
[fv-az1755-505:05427] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fbca54a5ff5]
[fv-az1755-505:05427] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fbca54bb0da]
[fv-az1755-505:05427] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fbca54a5a55]
[fv-az1755-505:05427] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fbca54a5a6f]
[fv-az1755-505:05427] [ 8] plumed_master(+0x146dd)[0x5573845d96dd]
[fv-az1755-505:05427] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fbca502a1ca]
[fv-az1755-505:05427] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fbca502a28b]
[fv-az1755-505:05427] [11] plumed_master(+0x15365)[0x5573845da365]
[fv-az1755-505:05427] *** End of error message ***
</pre>
{% endraw %}
