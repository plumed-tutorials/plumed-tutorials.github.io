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
[fv-az1315-757:08405] *** Process received signal ***
[fv-az1315-757:08405] Signal: Aborted (6)
[fv-az1315-757:08405] Signal code:  (-6)
[fv-az1315-757:08405] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4189e45330]
[fv-az1315-757:08405] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4189e9eb2c]
[fv-az1315-757:08405] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4189e4527e]
[fv-az1315-757:08405] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4189e288ff]
[fv-az1315-757:08405] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f418a2a5ff5]
[fv-az1315-757:08405] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f418a2bb0da]
[fv-az1315-757:08405] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f418a2a5a55]
[fv-az1315-757:08405] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f418a2a5a6f]
[fv-az1315-757:08405] [ 8] plumed(+0x13209)[0x560d4c573209]
[fv-az1315-757:08405] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4189e2a1ca]
[fv-az1315-757:08405] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4189e2a28b]
[fv-az1315-757:08405] [11] plumed(+0x134a5)[0x560d4c5734a5]
[fv-az1315-757:08405] *** End of error message ***
</pre>
{% endraw %}
