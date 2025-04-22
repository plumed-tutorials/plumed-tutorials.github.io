Stderr for source:  PIV-PathCV_meta.md_working_1.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label res : cannot find action named p1 (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[fv-az2211-783:05697] *** Process received signal ***
[fv-az2211-783:05697] Signal: Aborted (6)
[fv-az2211-783:05697] Signal code:  (-6)
[fv-az2211-783:05697] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe236645330]
[fv-az2211-783:05697] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe23669eb2c]
[fv-az2211-783:05697] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe23664527e]
[fv-az2211-783:05697] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe2366288ff]
[fv-az2211-783:05697] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe236aa5ff5]
[fv-az2211-783:05697] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe236abb0da]
[fv-az2211-783:05697] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe236aa5a55]
[fv-az2211-783:05697] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe236aa5a6f]
[fv-az2211-783:05697] [ 8] plumed_master(+0x146dd)[0x55a3024736dd]
[fv-az2211-783:05697] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe23662a1ca]
[fv-az2211-783:05697] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe23662a28b]
[fv-az2211-783:05697] [11] plumed_master(+0x15365)[0x55a302474365]
[fv-az2211-783:05697] *** End of error message ***
</pre>
{% endraw %}
