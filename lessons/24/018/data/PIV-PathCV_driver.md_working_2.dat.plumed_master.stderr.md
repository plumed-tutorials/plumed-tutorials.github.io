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
[pkrvmf6wy0o8zjz:58781] *** Process received signal ***
[pkrvmf6wy0o8zjz:58781] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58781] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58781] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fbe22e45330]
[pkrvmf6wy0o8zjz:58781] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fbe22e9eb2c]
[pkrvmf6wy0o8zjz:58781] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fbe22e4527e]
[pkrvmf6wy0o8zjz:58781] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fbe22e288ff]
[pkrvmf6wy0o8zjz:58781] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fbe232a5ff5]
[pkrvmf6wy0o8zjz:58781] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fbe232bb0da]
[pkrvmf6wy0o8zjz:58781] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fbe232a5a55]
[pkrvmf6wy0o8zjz:58781] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fbe232a5a6f]
[pkrvmf6wy0o8zjz:58781] [ 8] plumed_master(+0x146dd)[0x561a525876dd]
[pkrvmf6wy0o8zjz:58781] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fbe22e2a1ca]
[pkrvmf6wy0o8zjz:58781] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fbe22e2a28b]
[pkrvmf6wy0o8zjz:58781] [11] plumed_master(+0x15365)[0x561a52588365]
[pkrvmf6wy0o8zjz:58781] *** End of error message ***
</pre>
{% endraw %}
