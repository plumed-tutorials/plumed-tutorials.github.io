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
[pkrvmf6wy0o8zjz:61462] *** Process received signal ***
[pkrvmf6wy0o8zjz:61462] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61462] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61462] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fad2ca45330]
[pkrvmf6wy0o8zjz:61462] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fad2ca9eb2c]
[pkrvmf6wy0o8zjz:61462] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fad2ca4527e]
[pkrvmf6wy0o8zjz:61462] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fad2ca288ff]
[pkrvmf6wy0o8zjz:61462] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fad2cea5ff5]
[pkrvmf6wy0o8zjz:61462] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fad2cebb0da]
[pkrvmf6wy0o8zjz:61462] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fad2cea5a55]
[pkrvmf6wy0o8zjz:61462] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fad2cea5a6f]
[pkrvmf6wy0o8zjz:61462] [ 8] plumed(+0x13209)[0x55fb42f0f209]
[pkrvmf6wy0o8zjz:61462] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fad2ca2a1ca]
[pkrvmf6wy0o8zjz:61462] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fad2ca2a28b]
[pkrvmf6wy0o8zjz:61462] [11] plumed(+0x134a5)[0x55fb42f0f4a5]
[pkrvmf6wy0o8zjz:61462] *** End of error message ***
</pre>
{% endraw %}
