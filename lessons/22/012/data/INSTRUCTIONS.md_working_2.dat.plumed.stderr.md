Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action ENVIRONMENTSIMILARITY with label s : keyword SIGMA could not be read correctly
[fv-az2211-783:06048] *** Process received signal ***
[fv-az2211-783:06048] Signal: Aborted (6)
[fv-az2211-783:06048] Signal code:  (-6)
[fv-az2211-783:06048] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f865ee45330]
[fv-az2211-783:06048] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f865ee9eb2c]
[fv-az2211-783:06048] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f865ee4527e]
[fv-az2211-783:06048] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f865ee288ff]
[fv-az2211-783:06048] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f865f2a5ff5]
[fv-az2211-783:06048] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f865f2bb0da]
[fv-az2211-783:06048] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f865f2a5a55]
[fv-az2211-783:06048] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f865f2a5a6f]
[fv-az2211-783:06048] [ 8] plumed(+0x13209)[0x5627823d6209]
[fv-az2211-783:06048] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f865ee2a1ca]
[fv-az2211-783:06048] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f865ee2a28b]
[fv-az2211-783:06048] [11] plumed(+0x134a5)[0x5627823d64a5]
[fv-az2211-783:06048] *** End of error message ***
</pre>
{% endraw %}
