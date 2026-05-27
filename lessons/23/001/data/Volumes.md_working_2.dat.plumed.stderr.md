Stderr for source:  Volumes.md_working_2.dat   
Download: [zipped raw stdout](Volumes.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Volumes.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action INSPHERE with label sp : keyword DATA is compulsory for this action
[runnervmg397c:80451] *** Process received signal ***
[runnervmg397c:80451] Signal: Aborted (6)
[runnervmg397c:80451] Signal code:  (-6)
[runnervmg397c:80451] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5343445330]
[runnervmg397c:80451] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f534349eb2c]
[runnervmg397c:80451] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f534344527e]
[runnervmg397c:80451] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f53434288ff]
[runnervmg397c:80451] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f53438a5ff5]
[runnervmg397c:80451] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f53438bb0da]
[runnervmg397c:80451] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f53438a5a55]
[runnervmg397c:80451] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f53438a5a6f]
[runnervmg397c:80451] [ 8] plumed(+0x13209)[0x556bcd597209]
[runnervmg397c:80451] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f534342a1ca]
[runnervmg397c:80451] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f534342a28b]
[runnervmg397c:80451] [11] plumed(+0x134a5)[0x556bcd5974a5]
[runnervmg397c:80451] *** End of error message ***
</pre>
{% endraw %}
