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
[fv-az1315-757:08437] *** Process received signal ***
[fv-az1315-757:08437] Signal: Aborted (6)
[fv-az1315-757:08437] Signal code:  (-6)
[fv-az1315-757:08437] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9618a45330]
[fv-az1315-757:08437] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9618a9eb2c]
[fv-az1315-757:08437] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9618a4527e]
[fv-az1315-757:08437] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9618a288ff]
[fv-az1315-757:08437] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9618ea5ff5]
[fv-az1315-757:08437] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9618ebb0da]
[fv-az1315-757:08437] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9618ea5a55]
[fv-az1315-757:08437] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9618ea5a6f]
[fv-az1315-757:08437] [ 8] plumed(+0x13209)[0x560f3a655209]
[fv-az1315-757:08437] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9618a2a1ca]
[fv-az1315-757:08437] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9618a2a28b]
[fv-az1315-757:08437] [11] plumed(+0x134a5)[0x560f3a6554a5]
[fv-az1315-757:08437] *** End of error message ***
</pre>
{% endraw %}
