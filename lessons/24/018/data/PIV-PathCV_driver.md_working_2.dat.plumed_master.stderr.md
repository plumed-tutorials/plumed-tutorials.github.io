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
[runnervm3jyl0:79077] *** Process received signal ***
[runnervm3jyl0:79077] Signal: Aborted (6)
[runnervm3jyl0:79077] Signal code:  (-6)
[runnervm3jyl0:79077] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0cd3a45330]
[runnervm3jyl0:79077] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0cd3a9eb2c]
[runnervm3jyl0:79077] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0cd3a4527e]
[runnervm3jyl0:79077] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0cd3a288ff]
[runnervm3jyl0:79077] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0cd3ea5ff5]
[runnervm3jyl0:79077] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0cd3ebb0da]
[runnervm3jyl0:79077] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0cd3ea5a55]
[runnervm3jyl0:79077] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0cd3ea5a6f]
[runnervm3jyl0:79077] [ 8] plumed_master(+0x146dd)[0x55b4c16876dd]
[runnervm3jyl0:79077] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0cd3a2a1ca]
[runnervm3jyl0:79077] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0cd3a2a28b]
[runnervm3jyl0:79077] [11] plumed_master(+0x15365)[0x55b4c1688365]
[runnervm3jyl0:79077] *** End of error message ***
</pre>
{% endraw %}
