Stderr for source:  PIV-PathCV_driver.md_working_2.dat   
Download: [zipped raw stdout](PIV-PathCV_driver.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_driver.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action FUNCPATHMSD with label p1 : cannot find action named c1 (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[runnervm3jyl0:47164] *** Process received signal ***
[runnervm3jyl0:47164] Signal: Aborted (6)
[runnervm3jyl0:47164] Signal code:  (-6)
[runnervm3jyl0:47164] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5824845330]
[runnervm3jyl0:47164] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f582489eb2c]
[runnervm3jyl0:47164] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f582484527e]
[runnervm3jyl0:47164] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f58248288ff]
[runnervm3jyl0:47164] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f5824ca5ff5]
[runnervm3jyl0:47164] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f5824cbb0da]
[runnervm3jyl0:47164] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f5824ca5a55]
[runnervm3jyl0:47164] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f5824ca5a6f]
[runnervm3jyl0:47164] [ 8] plumed_master(+0x146dd)[0x556dca1bf6dd]
[runnervm3jyl0:47164] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f582482a1ca]
[runnervm3jyl0:47164] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f582482a28b]
[runnervm3jyl0:47164] [11] plumed_master(+0x15365)[0x556dca1c0365]
[runnervm3jyl0:47164] *** End of error message ***
</pre>
{% endraw %}
