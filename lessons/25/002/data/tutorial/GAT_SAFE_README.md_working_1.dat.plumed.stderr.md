Stderr for source:  tutorial/GAT_SAFE_README.md_working_1.dat   
Download: [zipped raw stdout](GAT_SAFE_README.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](GAT_SAFE_README.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: BAIES LABEL=baies ATOMS=batoms DATA_FILE=3-bAIes-setup/logn.out PRIOR=JEFFREYS TEMP=2.478541306
Maybe a missing space or a typo?
[runnervm3jyl0:46790] *** Process received signal ***
[runnervm3jyl0:46790] Signal: Aborted (6)
[runnervm3jyl0:46790] Signal code:  (-6)
[runnervm3jyl0:46790] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7efc6de45330]
[runnervm3jyl0:46790] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7efc6de9eb2c]
[runnervm3jyl0:46790] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7efc6de4527e]
[runnervm3jyl0:46790] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7efc6de288ff]
[runnervm3jyl0:46790] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7efc6e2a5ff5]
[runnervm3jyl0:46790] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7efc6e2bb0da]
[runnervm3jyl0:46790] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7efc6e2a5a55]
[runnervm3jyl0:46790] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7efc6e2a5a6f]
[runnervm3jyl0:46790] [ 8] plumed(+0x13209)[0x55ea99c3f209]
[runnervm3jyl0:46790] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7efc6de2a1ca]
[runnervm3jyl0:46790] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7efc6de2a28b]
[runnervm3jyl0:46790] [11] plumed(+0x134a5)[0x55ea99c3f4a5]
[runnervm3jyl0:46790] *** End of error message ***
</pre>
{% endraw %}
