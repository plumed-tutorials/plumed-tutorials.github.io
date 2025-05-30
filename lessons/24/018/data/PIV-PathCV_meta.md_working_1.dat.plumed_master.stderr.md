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
[pkrvmf6wy0o8zjz:59119] *** Process received signal ***
[pkrvmf6wy0o8zjz:59119] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59119] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59119] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ffb72a45330]
[pkrvmf6wy0o8zjz:59119] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ffb72a9eb2c]
[pkrvmf6wy0o8zjz:59119] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ffb72a4527e]
[pkrvmf6wy0o8zjz:59119] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ffb72a288ff]
[pkrvmf6wy0o8zjz:59119] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ffb72ea5ff5]
[pkrvmf6wy0o8zjz:59119] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ffb72ebb0da]
[pkrvmf6wy0o8zjz:59119] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ffb72ea5a55]
[pkrvmf6wy0o8zjz:59119] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ffb72ea5a6f]
[pkrvmf6wy0o8zjz:59119] [ 8] plumed_master(+0x146dd)[0x55cbbff3b6dd]
[pkrvmf6wy0o8zjz:59119] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ffb72a2a1ca]
[pkrvmf6wy0o8zjz:59119] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ffb72a2a28b]
[pkrvmf6wy0o8zjz:59119] [11] plumed_master(+0x15365)[0x55cbbff3c365]
[pkrvmf6wy0o8zjz:59119] *** End of error message ***
</pre>
{% endraw %}
