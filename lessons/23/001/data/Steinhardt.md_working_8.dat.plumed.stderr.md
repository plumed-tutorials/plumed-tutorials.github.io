Stderr for source:  Steinhardt.md_working_8.dat   
Download: [zipped raw stdout](Steinhardt.md_working_8.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_8.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[runnervmg397c:79744] *** Process received signal ***
[runnervmg397c:79744] Signal: Aborted (6)
[runnervmg397c:79744] Signal code:  (-6)
[runnervmg397c:79744] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f8084c45330]
[runnervmg397c:79744] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f8084c9eb2c]
[runnervmg397c:79744] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f8084c4527e]
[runnervmg397c:79744] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f8084c288ff]
[runnervmg397c:79744] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f80850a5ff5]
[runnervmg397c:79744] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f80850bb0da]
[runnervmg397c:79744] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f80850a5a55]
[runnervmg397c:79744] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f80850a5a6f]
[runnervmg397c:79744] [ 8] plumed(+0x13209)[0x561c012db209]
[runnervmg397c:79744] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f8084c2a1ca]
[runnervmg397c:79744] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f8084c2a28b]
[runnervmg397c:79744] [11] plumed(+0x134a5)[0x561c012db4a5]
[runnervmg397c:79744] *** End of error message ***
</pre>
{% endraw %}
