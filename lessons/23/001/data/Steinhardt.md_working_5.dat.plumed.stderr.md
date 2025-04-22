Stderr for source:  Steinhardt.md_working_5.dat   
Download: [zipped raw stdout](Steinhardt.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action PRINT with label @1 : action q4 has no component named q4 (hint! the components in this actions are: )
[fv-az1315-757:06423] *** Process received signal ***
[fv-az1315-757:06423] Signal: Aborted (6)
[fv-az1315-757:06423] Signal code:  (-6)
[fv-az1315-757:06423] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa903645330]
[fv-az1315-757:06423] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa90369eb2c]
[fv-az1315-757:06423] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa90364527e]
[fv-az1315-757:06423] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa9036288ff]
[fv-az1315-757:06423] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa903aa5ff5]
[fv-az1315-757:06423] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa903abb0da]
[fv-az1315-757:06423] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa903aa5a55]
[fv-az1315-757:06423] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa903aa5a6f]
[fv-az1315-757:06423] [ 8] plumed(+0x13209)[0x55902ba77209]
[fv-az1315-757:06423] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa90362a1ca]
[fv-az1315-757:06423] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa90362a28b]
[fv-az1315-757:06423] [11] plumed(+0x134a5)[0x55902ba774a5]
[fv-az1315-757:06423] *** End of error message ***
</pre>
{% endraw %}
