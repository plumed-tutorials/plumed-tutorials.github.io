Stderr for source:  histograms.md_working_8.dat   
Download: [zipped raw stdout](histograms.md_working_8.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_8.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCES with label d1 : keyword ATOMS could not be read correctly
[runnervmg397c:81135] *** Process received signal ***
[runnervmg397c:81135] Signal: Aborted (6)
[runnervmg397c:81135] Signal code:  (-6)
[runnervmg397c:81135] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f8834c45330]
[runnervmg397c:81135] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f8834c9eb2c]
[runnervmg397c:81135] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f8834c4527e]
[runnervmg397c:81135] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f8834c288ff]
[runnervmg397c:81135] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f88350a5ff5]
[runnervmg397c:81135] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f88350bb0da]
[runnervmg397c:81135] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f88350a5a55]
[runnervmg397c:81135] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f88350a5a6f]
[runnervmg397c:81135] [ 8] plumed(+0x13209)[0x5643c682b209]
[runnervmg397c:81135] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f8834c2a1ca]
[runnervmg397c:81135] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f8834c2a28b]
[runnervmg397c:81135] [11] plumed(+0x134a5)[0x5643c682b4a5]
[runnervmg397c:81135] *** End of error message ***
</pre>
{% endraw %}
