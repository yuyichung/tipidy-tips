* keyword arguments must follow non-keyword arguments \(e.g. var = \("a", b="b"\) instead of var = \(b="b", "a"\)\)

* If you do not file.flush\(\) after file.write\(\), and if you use subprocess.call\(stdout=file\), you will discover that the subprocess content is written before the file.write\(\) content because subprocess.call\(\) flushes



