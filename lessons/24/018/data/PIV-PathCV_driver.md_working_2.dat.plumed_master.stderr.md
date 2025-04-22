Stderr for source:  PIV-PathCV_driver.md_working_2.dat   
Download: [zipped raw stdout](PIV-PathCV_driver.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_driver.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action FUNCPATHMSD with label p1 : cannot find action named c1 (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[fv-az2211-783:05606] *** Process received signal ***
[fv-az2211-783:05606] Signal: Aborted (6)
[fv-az2211-783:05606] Signal code:  (-6)
[fv-az2211-783:05606] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f37a6e45330]
[fv-az2211-783:05606] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f37a6e9eb2c]
[fv-az2211-783:05606] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f37a6e4527e]
[fv-az2211-783:05606] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f37a6e288ff]
[fv-az2211-783:05606] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f37a72a5ff5]
[fv-az2211-783:05606] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f37a72bb0da]
[fv-az2211-783:05606] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f37a72a5a55]
[fv-az2211-783:05606] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f37a72a5a6f]
[fv-az2211-783:05606] [ 8] plumed_master(+0x146dd)[0x5571851096dd]
[fv-az2211-783:05606] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f37a6e2a1ca]
[fv-az2211-783:05606] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f37a6e2a28b]
[fv-az2211-783:05606] [11] plumed_master(+0x15365)[0x55718510a365]
[fv-az2211-783:05606] *** End of error message ***
</pre>
{% endraw %}
