Stderr for source:  INSTRUCTIONS.md_working_4.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[pkrvmf6wy0o8zjz:59646] *** Process received signal ***
[pkrvmf6wy0o8zjz:59646] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59646] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59646] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0519645330]
[pkrvmf6wy0o8zjz:59646] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f051969eb2c]
[pkrvmf6wy0o8zjz:59646] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f051964527e]
[pkrvmf6wy0o8zjz:59646] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f05196288ff]
[pkrvmf6wy0o8zjz:59646] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0519aa5ff5]
[pkrvmf6wy0o8zjz:59646] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0519abb0da]
[pkrvmf6wy0o8zjz:59646] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0519aa5a55]
[pkrvmf6wy0o8zjz:59646] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0519aa5a6f]
[pkrvmf6wy0o8zjz:59646] [ 8] plumed_master(+0x146dd)[0x55ec902816dd]
[pkrvmf6wy0o8zjz:59646] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f051962a1ca]
[pkrvmf6wy0o8zjz:59646] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f051962a28b]
[pkrvmf6wy0o8zjz:59646] [11] plumed_master(+0x15365)[0x55ec90282365]
[pkrvmf6wy0o8zjz:59646] *** End of error message ***
</pre>
{% endraw %}
