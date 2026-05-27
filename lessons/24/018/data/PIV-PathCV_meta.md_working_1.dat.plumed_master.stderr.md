Stderr for source:  PIV-PathCV_meta.md_working_1.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label res : cannot find action named p1 (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[runnervm3jyl0:79136] *** Process received signal ***
[runnervm3jyl0:79136] Signal: Aborted (6)
[runnervm3jyl0:79136] Signal code:  (-6)
[runnervm3jyl0:79136] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc774445330]
[runnervm3jyl0:79136] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc77449eb2c]
[runnervm3jyl0:79136] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc77444527e]
[runnervm3jyl0:79136] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc7744288ff]
[runnervm3jyl0:79136] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc7748a5ff5]
[runnervm3jyl0:79136] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc7748bb0da]
[runnervm3jyl0:79136] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc7748a5a55]
[runnervm3jyl0:79136] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc7748a5a6f]
[runnervm3jyl0:79136] [ 8] plumed_master(+0x146dd)[0x558e1b4266dd]
[runnervm3jyl0:79136] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc77442a1ca]
[runnervm3jyl0:79136] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc77442a28b]
[runnervm3jyl0:79136] [11] plumed_master(+0x15365)[0x558e1b427365]
[runnervm3jyl0:79136] *** End of error message ***
</pre>
{% endraw %}
