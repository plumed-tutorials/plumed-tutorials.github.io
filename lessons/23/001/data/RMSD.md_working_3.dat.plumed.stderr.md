Stderr for source:  RMSD.md_working_3.dat   
Download: [zipped raw stdout](RMSD.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(reference/MetricRegister.h:105) std::unique_ptr<_Tp> PLMD::MetricRegister::create(const std::string&, const PLMD::PDB&) [with T = PLMD::ReferenceConfiguration; std::string = std::__cxx11::basic_string<char>]
+++ assertion failed: rtype.length()>0
TYPE not specified in pdb input file
[runnervmg397c:81334] *** Process received signal ***
[runnervmg397c:81334] Signal: Aborted (6)
[runnervmg397c:81334] Signal code:  (-6)
[runnervmg397c:81334] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fea59a45330]
[runnervmg397c:81334] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fea59a9eb2c]
[runnervmg397c:81334] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fea59a4527e]
[runnervmg397c:81334] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fea59a288ff]
[runnervmg397c:81334] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fea59ea5ff5]
[runnervmg397c:81334] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fea59ebb0da]
[runnervmg397c:81334] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fea59ea5a55]
[runnervmg397c:81334] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fea59ea5a6f]
[runnervmg397c:81334] [ 8] plumed(+0x13209)[0x56534240b209]
[runnervmg397c:81334] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fea59a2a1ca]
[runnervmg397c:81334] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fea59a2a28b]
[runnervmg397c:81334] [11] plumed(+0x134a5)[0x56534240b4a5]
[runnervmg397c:81334] *** End of error message ***
</pre>
{% endraw %}
