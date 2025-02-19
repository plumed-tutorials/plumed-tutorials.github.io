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
[fv-az1755-505:08303] *** Process received signal ***
[fv-az1755-505:08303] Signal: Aborted (6)
[fv-az1755-505:08303] Signal code:  (-6)
[fv-az1755-505:08303] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2832845330]
[fv-az1755-505:08303] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f283289eb2c]
[fv-az1755-505:08303] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f283284527e]
[fv-az1755-505:08303] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f28328288ff]
[fv-az1755-505:08303] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2832ca5ff5]
[fv-az1755-505:08303] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2832cbb0da]
[fv-az1755-505:08303] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2832ca5a55]
[fv-az1755-505:08303] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2832ca5a6f]
[fv-az1755-505:08303] [ 8] plumed(+0x13209)[0x561631f9d209]
[fv-az1755-505:08303] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f283282a1ca]
[fv-az1755-505:08303] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f283282a28b]
[fv-az1755-505:08303] [11] plumed(+0x134a5)[0x561631f9d4a5]
[fv-az1755-505:08303] *** End of error message ***
</pre>
{% endraw %}
