Stderr for source:  work/plumed_ex11.dat   
Download: [zipped raw stdout](plumed_ex11.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex11.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @73 : keyword ARG is compulsory for this action
[runnervmg397c:79754] *** Process received signal ***
[runnervmg397c:79754] Signal: Aborted (6)
[runnervmg397c:79754] Signal code:  (-6)
[runnervmg397c:79754] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f07c8045330]
[runnervmg397c:79754] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f07c809eb2c]
[runnervmg397c:79754] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f07c804527e]
[runnervmg397c:79754] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f07c80288ff]
[runnervmg397c:79754] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f07c84a5ff5]
[runnervmg397c:79754] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f07c84bb0da]
[runnervmg397c:79754] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f07c84a5a55]
[runnervmg397c:79754] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f07c84a5a6f]
[runnervmg397c:79754] [ 8] plumed_master(+0x146dd)[0x55e66539b6dd]
[runnervmg397c:79754] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f07c802a1ca]
[runnervmg397c:79754] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f07c802a28b]
[runnervmg397c:79754] [11] plumed_master(+0x15365)[0x55e66539c365]
[runnervmg397c:79754] *** End of error message ***
</pre>
{% endraw %}
