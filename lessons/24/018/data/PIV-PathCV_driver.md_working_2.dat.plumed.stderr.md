Stderr for source:  PIV-PathCV_driver.md_working_2.dat   
Download: [zipped raw stdout](PIV-PathCV_driver.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_driver.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action FUNCPATHMSD with label p1 : cannot find action named c1 (hint! the actions with value in this ActionSet are: )
[fv-az2211-783:05590] *** Process received signal ***
[fv-az2211-783:05590] Signal: Aborted (6)
[fv-az2211-783:05590] Signal code:  (-6)
[fv-az2211-783:05590] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9e36645330]
[fv-az2211-783:05590] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9e3669eb2c]
[fv-az2211-783:05590] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9e3664527e]
[fv-az2211-783:05590] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9e366288ff]
[fv-az2211-783:05590] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9e36aa5ff5]
[fv-az2211-783:05590] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9e36abb0da]
[fv-az2211-783:05590] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9e36aa5a55]
[fv-az2211-783:05590] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9e36aa5a6f]
[fv-az2211-783:05590] [ 8] plumed(+0x13209)[0x557ee163a209]
[fv-az2211-783:05590] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9e3662a1ca]
[fv-az2211-783:05590] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9e3662a28b]
[fv-az2211-783:05590] [11] plumed(+0x134a5)[0x557ee163a4a5]
[fv-az2211-783:05590] *** End of error message ***
</pre>
{% endraw %}
