Stderr for source:  Volumes.md_working_1.dat   
Download: [zipped raw stdout](Volumes.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Volumes.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action INSPHERE with label sp : keyword DATA is compulsory for this action
[fv-az1755-505:07097] *** Process received signal ***
[fv-az1755-505:07097] Signal: Aborted (6)
[fv-az1755-505:07097] Signal code:  (-6)
[fv-az1755-505:07097] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff8c5645330]
[fv-az1755-505:07097] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff8c569eb2c]
[fv-az1755-505:07097] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff8c564527e]
[fv-az1755-505:07097] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff8c56288ff]
[fv-az1755-505:07097] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff8c5aa5ff5]
[fv-az1755-505:07097] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff8c5abb0da]
[fv-az1755-505:07097] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff8c5aa5a55]
[fv-az1755-505:07097] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff8c5aa5a6f]
[fv-az1755-505:07097] [ 8] plumed(+0x13209)[0x5618a6a9f209]
[fv-az1755-505:07097] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff8c562a1ca]
[fv-az1755-505:07097] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff8c562a28b]
[fv-az1755-505:07097] [11] plumed(+0x134a5)[0x5618a6a9f4a5]
[fv-az1755-505:07097] *** End of error message ***
</pre>
{% endraw %}
