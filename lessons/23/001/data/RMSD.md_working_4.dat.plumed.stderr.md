Stderr for source:  RMSD.md_working_4.dat   
Download: [zipped raw stdout](RMSD.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(reference/MetricRegister.h:105) std::unique_ptr<_Tp> PLMD::MetricRegister::create(const std::string&, const PLMD::PDB&) [with T = PLMD::ReferenceConfiguration; std::string = std::__cxx11::basic_string<char>]
+++ assertion failed: rtype.length()>0
TYPE not specified in pdb input file
[runnervm3jyl0:49337] *** Process received signal ***
[runnervm3jyl0:49337] Signal: Aborted (6)
[runnervm3jyl0:49337] Signal code:  (-6)
[runnervm3jyl0:49337] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f54e5245330]
[runnervm3jyl0:49337] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f54e529eb2c]
[runnervm3jyl0:49337] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f54e524527e]
[runnervm3jyl0:49337] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f54e52288ff]
[runnervm3jyl0:49337] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f54e56a5ff5]
[runnervm3jyl0:49337] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f54e56bb0da]
[runnervm3jyl0:49337] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f54e56a5a55]
[runnervm3jyl0:49337] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f54e56a5a6f]
[runnervm3jyl0:49337] [ 8] plumed(+0x13209)[0x558c9e60b209]
[runnervm3jyl0:49337] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f54e522a1ca]
[runnervm3jyl0:49337] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f54e522a28b]
[runnervm3jyl0:49337] [11] plumed(+0x134a5)[0x558c9e60b4a5]
[runnervm3jyl0:49337] *** End of error message ***
</pre>
{% endraw %}
