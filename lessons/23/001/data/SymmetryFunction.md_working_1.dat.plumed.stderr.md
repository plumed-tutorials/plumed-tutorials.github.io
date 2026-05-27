Stderr for source:  SymmetryFunction.md_working_1.dat   
Download: [zipped raw stdout](SymmetryFunction.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](SymmetryFunction.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label c1 : No atoms have been read in
[runnervmg397c:80489] *** Process received signal ***
[runnervmg397c:80489] Signal: Aborted (6)
[runnervmg397c:80489] Signal code:  (-6)
[runnervmg397c:80489] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3f8a045330]
[runnervmg397c:80489] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3f8a09eb2c]
[runnervmg397c:80489] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3f8a04527e]
[runnervmg397c:80489] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3f8a0288ff]
[runnervmg397c:80489] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f3f8a4a5ff5]
[runnervmg397c:80489] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f3f8a4bb0da]
[runnervmg397c:80489] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f3f8a4a5a55]
[runnervmg397c:80489] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f3f8a4a5a6f]
[runnervmg397c:80489] [ 8] plumed(+0x13209)[0x5642862ae209]
[runnervmg397c:80489] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3f8a02a1ca]
[runnervmg397c:80489] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3f8a02a28b]
[runnervmg397c:80489] [11] plumed(+0x134a5)[0x5642862ae4a5]
[runnervmg397c:80489] *** End of error message ***
</pre>
{% endraw %}
