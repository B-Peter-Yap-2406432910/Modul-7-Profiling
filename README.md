# Profiling JMeter
### Notes: NUMBER_OF_STUDENTS saya turunkan menjadi 10_000 karena waktu eksekusi yang terlalu lama
##  /all-student

### GUI
![testResult_gui_all-student1.png](testResult/testResult_gui_all-student1.png)
![testResult_gui_all-student2.png](testResult/testResult_gui_all-student2.png)
![testResult_gui_all-student3.png](testResult/testResult_gui_all-student3.png)
![testResult_gui_all-student4.png](testResult/testResult_gui_all-student4.png)
### CLI
#### Before Optimization
![testResult_cli_all-student.png](testResult/testResult_cli_all-student.png)

#### After Optimization
![testResult_cli_all-student-optimized.png](testResult/testResult_cli_all-student-optimized.png)

## /all-student-name

### GUI
![testResult_gui_all-student-name1.png](testResult/testResult_gui_all-student-name1.png)
![testResult_gui_all-student-name2.png](testResult/testResult_gui_all-student-name2.png)
![testResult_gui_all-student-name3.png](testResult/testResult_gui_all-student-name3.png)
![testResult_gui_all-student-name4.png](testResult/testResult_gui_all-student-name4.png)
### CLI
#### Before Optimization
![testResult_cli_all-student-name.png](testResult/testResult_cli_all-student-name.png)
#### After Optimization
![testResult_cli_all-student-name-optimized.png](testResult/testResult_cli_all-student-name-optimized.png)

## /highest-gpa

### GUI
![testResult_gui_higest-gpa1.png](testResult/testResult_gui_higest-gpa1.png)
![testResult_gui_higest-gpa2.png](testResult/testResult_gui_higest-gpa2.png)
![testResult_gui_higest-gpa3.png](testResult/testResult_gui_higest-gpa3.png)
![testResult_gui_higest-gpa4.png](testResult/testResult_gui_higest-gpa4.png)

### CLI
#### Before Optimization
![testResult_cli_highest-gpa.png](testResult/testResult_cli_highest-gpa.png)
#### After Optimization
![testResult_cli_highest-gpa-optimized.png](testResult/testResult_cli_highest-gpa-optimized.png)


# Reflection

1. What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?
   - Jmeter adalah performance testing yang mengevaluasi performa aplikasi secara keseluruhannya saat menerima beban workload sedangkan Intellij Profiler adalah performance 
   testing yang mengevaluasi performa di level code. Dengan JMeter, kita bisa tahu informasi statistik dari server target (e.g response times, throughput, error percentage, etc) sedangkan 
   intellij profiller memberi kita informasi tentang seberapa lama latency dari tiap code yang memungkinkan kita bisa mengetahui code mana yang menimbulkan bottleneck.
2. How does the profiling process help you in identifying and understanding the weak points in your application?
   - Profiling memberikan bukti berupa data tentang cara kerja internal aplikasi yang kita buat saat dijalankan. Dari data ini, kita tidak perlu ribet-ribet melakukan tracing 
   di bagian mana code kita yang kurang teroptimisasi sehingga kita bisa lebih hemat waktu dan tenaga.
3. Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?
   - Ya, dengan mengetahui data tentang cpu time yang dihasilkan untuk masing-masing function call maka akan mempermudah saya menemukan bagian mana yang menjadi masalahnya
4. What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?
   - Menurut saya ada di menunggu karena semakin besar data dan app yang ada di suatu app maka akan semakin lama untuk test tersebut selesai. bahkan untuk test 1 kali di tutorial ini saja sudah memakan kira-kira
   30 menit untuk saya
5. What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?
   - Mungkin karena fungsi built-in langsung dari IDEnya, jadi lebih simpel dan tidak perlu menggunakan third party app lagi. lalu juga profiller ini sudah memberikan data yang lebih dari cukup bagi developer untuk tahu dimana letak
   function code yang memberikan bottleneck atau eksekusi yang paling lama.
6. How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?
   - Keduanya alat ini memang berjalan di scope yang berbeda maka wajar kalau performanya kadang tidak konsisten. Karena JMeter merupakan performa asli yang digunakan oleh user, maka saya akan prefer gunakan jmeter sebagai baseline saya. Jika memang ada yang perlu dioptimize, maka saya akan baru gunakan intellij profiller untuk menentukan letak 
   yang perlu dioptimisasi. keduanya memang berjalan saling melengkapi sehingga tidak mungkin juga untuk menggunakan 1 alat saja sebagai patokan dari setiap kondisi.
7. What strategies do you implement in optimizing application code after analyzing results
   from performance testing and profiling? How do you ensure the changes you make do
   not affect the application's functionality?
   - Pertama lihat dulu Jmeter untuk waktu eksekusi appnya lalu gunakan profiller untuk pinpoint letak yang perlu di optimize. Then gunakan test seperti unit test dan functional test untuk mendetermine apakah perubahan yang kita lakukan merubah fungsi dari appnya.





