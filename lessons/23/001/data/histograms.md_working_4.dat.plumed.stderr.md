Stderr for source:  histograms.md_working_4.dat   
Download: [zipped raw stdout](histograms.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[runnervmg397c:80992] *** Process received signal ***
[runnervmg397c:80992] Signal: Aborted (6)
[runnervmg397c:80992] Signal code:  (-6)
[runnervmg397c:80992] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0e75445330]
[runnervmg397c:80992] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0e7549eb2c]
[runnervmg397c:80992] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0e7544527e]
[runnervmg397c:80992] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0e754288ff]
[runnervmg397c:80992] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0e758a5ff5]
[runnervmg397c:80992] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0e758bb0da]
[runnervmg397c:80992] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0e758a5a55]
[runnervmg397c:80992] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0e758a5a6f]
[runnervmg397c:80992] [ 8] plumed(+0x13209)[0x55bef885e209]
[runnervmg397c:80992] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0e7542a1ca]
[runnervmg397c:80992] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0e7542a28b]
[runnervmg397c:80992] [11] plumed(+0x134a5)[0x55bef885e4a5]
[runnervmg397c:80992] *** End of error message ***
</pre>
{% endraw %}
