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
[pkrvmf6wy0o8zjz:61679] *** Process received signal ***
[pkrvmf6wy0o8zjz:61679] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61679] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61679] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1a28a45330]
[pkrvmf6wy0o8zjz:61679] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1a28a9eb2c]
[pkrvmf6wy0o8zjz:61679] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1a28a4527e]
[pkrvmf6wy0o8zjz:61679] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1a28a288ff]
[pkrvmf6wy0o8zjz:61679] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1a28ea5ff5]
[pkrvmf6wy0o8zjz:61679] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1a28ebb0da]
[pkrvmf6wy0o8zjz:61679] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1a28ea5a55]
[pkrvmf6wy0o8zjz:61679] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1a28ea5a6f]
[pkrvmf6wy0o8zjz:61679] [ 8] plumed(+0x13209)[0x56424cd1d209]
[pkrvmf6wy0o8zjz:61679] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1a28a2a1ca]
[pkrvmf6wy0o8zjz:61679] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1a28a2a28b]
[pkrvmf6wy0o8zjz:61679] [11] plumed(+0x134a5)[0x56424cd1d4a5]
[pkrvmf6wy0o8zjz:61679] *** End of error message ***
</pre>
{% endraw %}
