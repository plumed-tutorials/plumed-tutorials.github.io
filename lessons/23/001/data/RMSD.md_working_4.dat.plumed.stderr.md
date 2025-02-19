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
[fv-az1755-505:08334] *** Process received signal ***
[fv-az1755-505:08334] Signal: Aborted (6)
[fv-az1755-505:08334] Signal code:  (-6)
[fv-az1755-505:08334] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb2cba45330]
[fv-az1755-505:08334] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb2cba9eb2c]
[fv-az1755-505:08334] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb2cba4527e]
[fv-az1755-505:08334] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb2cba288ff]
[fv-az1755-505:08334] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb2cbea5ff5]
[fv-az1755-505:08334] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb2cbebb0da]
[fv-az1755-505:08334] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb2cbea5a55]
[fv-az1755-505:08334] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb2cbea5a6f]
[fv-az1755-505:08334] [ 8] plumed(+0x13209)[0x55f3d0b9f209]
[fv-az1755-505:08334] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb2cba2a1ca]
[fv-az1755-505:08334] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb2cba2a28b]
[fv-az1755-505:08334] [11] plumed(+0x134a5)[0x55f3d0b9f4a5]
[fv-az1755-505:08334] *** End of error message ***
</pre>
{% endraw %}
