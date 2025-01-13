#### 1.2 Naming numerous bits

Modern computers may store large amounts of data, such as thousands, millions, billions, or even trillions of bits.  
**Example:** A smartphone's memory (used by apps when running) may consist of about 1 billion bits, typically written as 1 gigabit or 1 Gb. In the metric system, the prefix "giga" means billion. Common metric prefixes are kilo (thousand), mega (million), giga (billion), and tera (trillion).

Just as humans commonly use powers of 10, computers commonly use powers of 2. A reason is because, just like neighborhoods use decimal addresses for house locations, storage devices use binary addresses for data locations. A binary address' range is a power of 2, such as \(2^{30}\) bits representing \(2^{30}\) addresses. That number equals 1,073,741,824, which is very close to 1 billion, so for convenience people commonly refer to that number of bits as 1 gigabit.

But using metric prefixes for computers is not accurate. Alternative prefixes, known as **IEC prefixes**, exist like kibi (\(2^{10}\) or 1024), mebi (\(2^{20}\) or 1,048,576), gibi (\(2^{30}\) or 1,073,741,824), and tebi (\(2^{40}\) or 1,099,511,627,776). In gibi, the "gi" refers to the metric prefix giga, and the "bi" to "binary". A gibi is abbreviated Gi, as in 1 Gi for 1 Gibibit. Likewise for other IEC prefixes.

When metric prefixes are used as in 1 Gigabit, computer folks understand those prefixes are informal and actually refer to the nearest power of 2.

---

#### Table 1.2.1: Powers of 2, and common metric and IEC prefixes for bits used near a thousand, million, and billion. Powers of 2 to the 16 and 32 are common so are listed too.

| Power of 2 | Value       | Metric Prefix for Bits (Informal)              | IEC Prefix for Bits             |
|------------|-------------|-----------------------------------------------|----------------------------------|
| 1          | 2           |                                               |                                  |
| 2          | 4           |                                               |                                  |
| 3          | 8           |                                               |                                  |
| 4          | 16          |                                               |                                  |
| 5          | 32          |                                               |                                  |
| 6          | 64          |                                               |                                  |
| 7          | 128         |                                               |                                  |
| 8          | 256         |                                               |                                  |
| 9          | 512         |                                               |                                  |
| 10         | 1024        | kilo (K): 1 kilobit or 1 Kb                   | kibi (Ki): 1 kibibit or 1 Kib   |
| 11         | 2048        |                                               |                                  |
| 12         | 4096        |                                               |                                  |
| 13         | 8192        |                                               |                                  |
| 14         | 16384       |                                               |                                  |
| 15         | 32768       |                                               |                                  |
| 16         | 65536       | 64 Kb                                         | 64 Kib                          |
| 17         | 131072      |                                               |                                  |
| 18         | 262144      |                                               |                                  |
| 19         | 524288      |                                               |                                  |
| 20         | 1048576     | mega (M): 1 megabit or 1 Mb                   | mebi (Mi): 1 mebibit or 1 Mib   |
| 21         | 2097152     |                                               |                                  |
| 22         | 4194304     |                                               |                                  |
| 23         | 8388608     |                                               |                                  |
| 24         | 16777216    |                                               |                                  |
| 25         | 33554432    |                                               |                                  |
| 26         | 67108864    |                                               |                                  |
| 27         | 134217728   |                                               |                                  |
| 28         | 268435456   |                                               |                                  |
| 29         | 536870912   |                                               |                                  |
| 30         | 1073741824  | giga (G): 1 gigabit or 1 Gb                   | gibi (Gi): 1 gibibit or 1 Gib   |
| 31         | 2147483648  |                                               |                                  |
| 32         | 4294967296  | 4 Gb                                          | 4 Gib                           |

---

Sizes often refer to **bytes** rather than bits, as in 128 gigabytes. The abbreviation uses a **B** rather than **b**, as in 128 GB rather than 128 Gb.

To help remember the relation of powers of two and powers of ten, one may note that \(2^{10}\) is near a thousand, \(2^{20}\) is near a million, and \(2^{30}\) is near a billion.


___________________________________

#### 1.2.1: Metric and IEC prefixes

1) 1024 bits using the metric prefix is informally written 1 Kb. Write 4096 bits informally using the metric prefix.
- [x] 4 Kb
- [ ] 4 Gb
- [ ] 4 MiB
- [ ] 4 KiB

2) \(2^{30}\) is close to one billion. Write \(2^{30}\) informally using a metric prefix.
- [x] 1 Gb
- [ ] 1 GiB
- [ ] 1 Kb
- [ ] 1 KiB

3) \(2^{32}\) is a common value in computers. Write \(2^{32}\) bits informally using an informal metric prefix.
- [x] 4 Gb
- [ ] 4 KiB
- [ ] 4 MiB
- [ ] 4 GiB

4) 1024 bits using the IEC prefix is written 1 Kib. Write 4096 bits using the IEC prefix.
- [x] 4 Kib
- [ ] 4 Kb
- [ ] 4 MiB
- [ ] 4 Gb

5) \(2^{30}\) is close to one billion. Write \(2^{30}\) using the IEC prefix.
- [x] 1 Gib
- [ ] 1 Gb
- [ ] 1 KiB
- [ ] 1 MiB

6) \(2^{32}\) is a common value in computers. Write \(2^{32}\) bits using the IEC prefix.
- [x] 4 Gib
- [ ] 4 GiB
- [ ] 4 Gb
- [ ] 4 Kb

7) Sizes are often written using bytes rather than bits. Write \(2^{16}\) bytes using an IEC prefix.
- [x] 64 KiB
- [ ] 64 Kb
- [ ] 64 GiB
- [ ] 64 MiB

___________________________________

#### Explanation Q1, 4 Kb
- K is short for kilo which means 1000. The b means bits. 4 Kb thus literally means 4000 bits, but it is known to actually mean 4096 bits.

#### Explanation Q2, 1 Gb
- G is short for giga which means billion. 1 Gb is known to be slightly more than 1 billion.

#### Explanation Q3, 4 Gb
- The nearest prefix is for one billion (which is near \(2^{30}\)). \(2^{32}\) is 4 times more so is written as 4 Gb. Computer folks know 4 Gb is actually slightly more than 4 billion.

#### Explanation Q4, 4 Kib
- 1024 bits is 1 Kib, so 4096 bits is 4 Kib.

#### Explanation Q5, 1 Gib
- Gi is short for gibi which means \(2^{30}\), b means bit. So 1 Gib is \(2^{30}\) bits, which is actually 1,073,741,824 bits.

#### Explanation Q6, 4 Gib
- \(2^{32}\) is 4 times more, so is written as 4 Gib, which is actually 4,294,967,296 bits.

#### Explanation Q7, 64 KiB
- A KiB is a kibibyte. 64 KiB is 65,536 bytes. The uppercase B means byte, vs. lowercase b for bit.

___________________________________

- IEC prefixes
https://physics.nist.gov/cuu/Units/binary.html