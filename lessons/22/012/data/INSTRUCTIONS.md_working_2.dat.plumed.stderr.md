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
[fv-az1690-151:05952] *** Process received signal ***
[fv-az1690-151:05952] Signal: Aborted (6)
[fv-az1690-151:05952] Signal code:  (-6)
[fv-az1690-151:05952] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd76a845330]
[fv-az1690-151:05952] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd76a89eb2c]
[fv-az1690-151:05952] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd76a84527e]
[fv-az1690-151:05952] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd76a8288ff]
[fv-az1690-151:05952] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd76aca5ff5]
[fv-az1690-151:05952] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd76acbb0da]
[fv-az1690-151:05952] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd76aca5a55]
[fv-az1690-151:05952] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd76aca5a6f]
[fv-az1690-151:05952] [ 8] plumed(+0x13209)[0x563402e11209]
[fv-az1690-151:05952] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd76a82a1ca]
[fv-az1690-151:05952] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd76a82a28b]
[fv-az1690-151:05952] [11] plumed(+0x134a5)[0x563402e114a5]
[fv-az1690-151:05952] *** End of error message ***
</pre>
{% endraw %}
