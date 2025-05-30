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
[pkrvmf6wy0o8zjz:59046] *** Process received signal ***
[pkrvmf6wy0o8zjz:59046] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59046] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59046] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7efdb3045330]
[pkrvmf6wy0o8zjz:59046] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7efdb309eb2c]
[pkrvmf6wy0o8zjz:59046] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7efdb304527e]
[pkrvmf6wy0o8zjz:59046] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7efdb30288ff]
[pkrvmf6wy0o8zjz:59046] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7efdb34a5ff5]
[pkrvmf6wy0o8zjz:59046] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7efdb34bb0da]
[pkrvmf6wy0o8zjz:59046] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7efdb34a5a55]
[pkrvmf6wy0o8zjz:59046] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7efdb34a5a6f]
[pkrvmf6wy0o8zjz:59046] [ 8] plumed(+0x13209)[0x5586a00fd209]
[pkrvmf6wy0o8zjz:59046] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7efdb302a1ca]
[pkrvmf6wy0o8zjz:59046] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7efdb302a28b]
[pkrvmf6wy0o8zjz:59046] [11] plumed(+0x134a5)[0x5586a00fd4a5]
[pkrvmf6wy0o8zjz:59046] *** End of error message ***
</pre>
{% endraw %}
