---
layout: post
title:  "Big-o"
date:   2018-06-24 17:30:00 +0900
categories: algorithm
tag:
- algorithm
comments : true
---

# Know Thy Complexities

Hi there!  This webpage covers the space and time Big-O complexities of common algorithms used in Computer Science.  When preparing for technical interviews in the past, I found myself spending hours crawling the internet putting together the best, average, and worst case complexities for search and sorting algorithms so that I wouldn't be stumped when asked about them.  Over the last few years, I've interviewed at several Silicon Valley startups, and also some bigger companies, like Google, Facebook, Yahoo, LinkedIn, and eBay, and each time that I prepared for an interview, I thought to myself "Why hasn't someone created a nice Big-O cheat sheet?".  So, to save all of you fine folks a ton of time, I went ahead and created one.  Enjoy! - [Eric](https://twitter.com/ericdrowell)

## Big-O Complexity Chart
![o](assets/img/big-o.png)
<p><span style="font-size: 16px; line-height: 28px;">보통 O(n^2)이상의 복잡도를 가지는 알고리즘은 좋지 않다.</span></p><p><span style="font-size: 16px; line-height: 28px;">$$ O(1) &lt; O(log n) &lt; O(n) &lt; O(nlog n) &lt; O(n^2) &lt; O(n^3) &lt; O(2^n) &lt; O(n!) $$</span></p><p><span style="font-size: 16px; line-height: 28px;"><br /></span></p><p style="text-align: center; clear: none; float: none;"><span class="imageblock" style="display:inline-block;width:530px;;height:auto;max-width:100%"><img src="https://t1.daumcdn.net/cfile/tistory/260F4850559AB6672C" style="max-width:100%;height:auto" width="530" height="359" filename="big_o_notation.png" filemime="image/jpeg"/></span></p><p><span style="font-size: 16px; line-height: 28px;"><br /></span></p><p><b style="font-size: 18.6666660308838px; line-height: 28px;"><u>빅오를 이용한 성능 비교</u></b></p><p><table class="txc-table" width="714" cellspacing="0" cellpadding="0" border="0" style="border:none;border-collapse:collapse;;font-family:돋움;font-size:12px"><tbody><tr><td style="width:238;height:24;border-bottom:1px solid #ccc;border-right:1px solid #ccc;border-top:1px solid #ccc;border-left:1px solid #ccc;;"><p style="text-align: center;"><span style="font-size: 16px; line-height: 24px;">n</span></p></td>
<td style="width:238;height:24;border-bottom:1px solid #ccc;border-right:1px solid #ccc;border-top:1px solid #ccc;;"><p style="text-align: center;"><span style="font-size: 12pt;">$O(n) $</span></p></td>
<td style="width:238;height:24;border-bottom:1px solid #ccc;border-right:1px solid #ccc;border-top:1px solid #ccc;;"><p style="text-align: center;"><span style="font-size: 12pt;">$O(logn) $</span></p></td>
</tr>
<tr><td style="width: 238px; height: 25px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(204, 204, 204); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(204, 204, 204); border-left-width: 1px; border-left-style: solid; border-left-color: rgb(204, 204, 204);"><p style="text-align: center;"><span style="font-size: 12pt;">500</span></p></td>
<td style="width: 238px; height: 25px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(204, 204, 204); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(204, 204, 204);"><p style="text-align: center;"><span style="font-size: 12pt;">500</span><span style="font-size: 12pt;">&nbsp;</span></p></td>
<td style="width: 238px; height: 25px; border-bottom-width: 1px; border-bottom-style: solid; border-bottom-color: rgb(204, 204, 204); border-right-width: 1px; border-right-style: solid; border-right-color: rgb(204, 204, 204);"><p style="text-align: center;"><span style="font-size: 12pt;">9&nbsp;</span></p></td>
</tr>
<tr><td style="width:238;height:24;border-bottom:1px solid #ccc;border-right:1px solid #ccc;border-left:1px solid #ccc;;"><p style="text-align: center;"><span style="font-size: 12pt;">5,000</span></p></td>
<td style="width:238;height:24;border-bottom:1px solid #ccc;border-right:1px solid #ccc;;"><p style="text-align: center;"><span style="font-size: 12pt;">5,000&nbsp;</span></p></td>
<td style="width:238;height:24;border-bottom:1px solid #ccc;border-right:1px solid #ccc;;"><p style="text-align: center;"><span style="font-size: 12pt;">13</span></p></td>
</tr>
<tr><td style="width:238;height:24;border-bottom:1px solid #ccc;border-right:1px solid #ccc;border-left:1px solid #ccc;;"><p style="text-align: center;"><span style="font-size: 12pt;">50,000</span></p></td>
<td style="width:238;height:24;border-bottom:1px solid #ccc;border-right:1px solid #ccc;;"><p style="text-align: center;"><span style="font-size: 12pt;">50,000</span></p></td>
<td style="width:238;height:24;border-bottom:1px solid #ccc;border-right:1px solid #ccc;;"><p style="text-align: center;"><span style="font-size: 12pt;">16</span></p></td>
</tr>
</tbody></table></p><p><span style="font-size: 12pt;"><u></u>

## Common Data Structure Operations

| Data Structure                                               | Time Complexity | Space Complexity |             |             |             |             |             |             |               |
| ------------------------------------------------------------ | --------------- | ---------------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ------------- |
|                                                              | Average         | Worst            | Worst       |             |             |             |             |             |               |
|                                                              | Access          | Search           | Insertion   | Deletion    | Access      | Search      | Insertion   | Deletion    |               |
| [Array](http://en.wikipedia.org/wiki/Array_data_structure)   | `Θ(1)`          | `Θ(n)`           | `Θ(n)`      | `Θ(n)`      | `O(1)`      | `O(n)`      | `O(n)`      | `O(n)`      | `O(n)`        |
| [Stack](http://en.wikipedia.org/wiki/Stack_(abstract_data_type)) | `Θ(n)`          | `Θ(n)`           | `Θ(1)`      | `Θ(1)`      | `O(n)`      | `O(n)`      | `O(1)`      | `O(1)`      | `O(n)`        |
| [Queue](http://en.wikipedia.org/wiki/Queue_(abstract_data_type)) | `Θ(n)`          | `Θ(n)`           | `Θ(1)`      | `Θ(1)`      | `O(n)`      | `O(n)`      | `O(1)`      | `O(1)`      | `O(n)`        |
| [Singly-Linked List](http://en.wikipedia.org/wiki/Singly_linked_list#Singly_linked_lists) | `Θ(n)`          | `Θ(n)`           | `Θ(1)`      | `Θ(1)`      | `O(n)`      | `O(n)`      | `O(1)`      | `O(1)`      | `O(n)`        |
| [Doubly-Linked List](http://en.wikipedia.org/wiki/Doubly_linked_list) | `Θ(n)`          | `Θ(n)`           | `Θ(1)`      | `Θ(1)`      | `O(n)`      | `O(n)`      | `O(1)`      | `O(1)`      | `O(n)`        |
| [Skip List](http://en.wikipedia.org/wiki/Skip_list)          | `Θ(log(n))`     | `Θ(log(n))`      | `Θ(log(n))` | `Θ(log(n))` | `O(n)`      | `O(n)`      | `O(n)`      | `O(n)`      | `O(n log(n))` |
| [Hash Table](http://en.wikipedia.org/wiki/Hash_table)        | `N/A`           | `Θ(1)`           | `Θ(1)`      | `Θ(1)`      | `N/A`       | `O(n)`      | `O(n)`      | `O(n)`      | `O(n)`        |
| [Binary Search Tree](http://en.wikipedia.org/wiki/Binary_search_tree) | `Θ(log(n))`     | `Θ(log(n))`      | `Θ(log(n))` | `Θ(log(n))` | `O(n)`      | `O(n)`      | `O(n)`      | `O(n)`      | `O(n)`        |
| [Cartesian Tree](https://en.wikipedia.org/wiki/Cartesian_tree) | `N/A`           | `Θ(log(n))`      | `Θ(log(n))` | `Θ(log(n))` | `N/A`       | `O(n)`      | `O(n)`      | `O(n)`      | `O(n)`        |
| [B-Tree](http://en.wikipedia.org/wiki/B_tree)                | `Θ(log(n))`     | `Θ(log(n))`      | `Θ(log(n))` | `Θ(log(n))` | `O(log(n))` | `O(log(n))` | `O(log(n))` | `O(log(n))` | `O(n)`        |
| [Red-Black Tree](http://en.wikipedia.org/wiki/Red-black_tree) | `Θ(log(n))`     | `Θ(log(n))`      | `Θ(log(n))` | `Θ(log(n))` | `O(log(n))` | `O(log(n))` | `O(log(n))` | `O(log(n))` | `O(n)`        |
| [Splay Tree](https://en.wikipedia.org/wiki/Splay_tree)       | `N/A`           | `Θ(log(n))`      | `Θ(log(n))` | `Θ(log(n))` | `N/A`       | `O(log(n))` | `O(log(n))` | `O(log(n))` | `O(n)`        |
| [AVL Tree](http://en.wikipedia.org/wiki/AVL_tree)            | `Θ(log(n))`     | `Θ(log(n))`      | `Θ(log(n))` | `Θ(log(n))` | `O(log(n))` | `O(log(n))` | `O(log(n))` | `O(log(n))` | `O(n)`        |
| [KD Tree](http://en.wikipedia.org/wiki/K-d_tree)             | `Θ(log(n))`     | `Θ(log(n))`      | `Θ(log(n))` | `Θ(log(n))` | `O(n)`      | `O(n)`      | `O(n)`      | `O(n)`      | `O(n)`        |

## Array Sorting Algorithms

| Algorithm                                                    | Time Complexity | Space Complexity |                  |             |
| ------------------------------------------------------------ | --------------- | ---------------- | ---------------- | ----------- |
|                                                              | Best            | Average          | Worst            | Worst       |
| [Quicksort](http://en.wikipedia.org/wiki/Quicksort)          | `Ω(n log(n))`   | `Θ(n log(n))`    | `O(n^2)`         | `O(log(n))` |
| [Mergesort](http://en.wikipedia.org/wiki/Merge_sort)         | `Ω(n log(n))`   | `Θ(n log(n))`    | `O(n log(n))`    | `O(n)`      |
| [Timsort](http://en.wikipedia.org/wiki/Timsort)              | `Ω(n)`          | `Θ(n log(n))`    | `O(n log(n))`    | `O(n)`      |
| [Heapsort](http://en.wikipedia.org/wiki/Heapsort)            | `Ω(n log(n))`   | `Θ(n log(n))`    | `O(n log(n))`    | `O(1)`      |
| [Bubble Sort](http://en.wikipedia.org/wiki/Bubble_sort)      | `Ω(n)`          | `Θ(n^2)`         | `O(n^2)`         | `O(1)`      |
| [Insertion Sort](http://en.wikipedia.org/wiki/Insertion_sort) | `Ω(n)`          | `Θ(n^2)`         | `O(n^2)`         | `O(1)`      |
| [Selection Sort](http://en.wikipedia.org/wiki/Selection_sort) | `Ω(n^2)`        | `Θ(n^2)`         | `O(n^2)`         | `O(1)`      |
| [Tree Sort](https://en.wikipedia.org/wiki/Tree_sort)         | `Ω(n log(n))`   | `Θ(n log(n))`    | `O(n^2)`         | `O(n)`      |
| [Shell Sort](http://en.wikipedia.org/wiki/Shellsort)         | `Ω(n log(n))`   | `Θ(n(log(n))^2)` | `O(n(log(n))^2)` | `O(1)`      |
| [Bucket Sort](http://en.wikipedia.org/wiki/Bucket_sort)      | `Ω(n+k)`        | `Θ(n+k)`         | `O(n^2)`         | `O(n)`      |
| [Radix Sort](http://en.wikipedia.org/wiki/Radix_sort)        | `Ω(nk)`         | `Θ(nk)`          | `O(nk)`          | `O(n+k)`    |
| [Counting Sort](https://en.wikipedia.org/wiki/Counting_sort) | `Ω(n+k)`        | `Θ(n+k)`         | `O(n+k)`         | `O(k)`      |
| [Cubesort](https://en.wikipedia.org/wiki/Cubesort)           | `Ω(n)`          | `Θ(n log(n))`    | `O(n log(n))`    | `O(n)`      |

## Learn More

- [Cracking the Coding Interview: 150 Programming Questions and Solutions](https://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X/ref=as_li_ss_tl?ie=UTF8&redirect=true&ref_=as_li_tl&linkCode=ll1&tag=bigocheatsheet-1-20&linkId=52f670296578886d22cacce6c054edff)
- [Introduction to Algorithms, 3rd Edition](https://www.amazon.com/Introduction-Algorithms-3rd-MIT-Press/dp/0262033844/ref=as_li_ss_tl?ie=UTF8&redirect=true&ref_=as_li_tl&linkCode=ll1&tag=bigocheatsheet-1-20&linkId=105e776075c7c7a38c9b0581586d1fa5)
- [Data Structures and Algorithms in Java (2nd Edition)](https://www.amazon.com/Data-Structures-Algorithms-Java-2nd/dp/0672324539/ref=as_li_ss_tl?ie=UTF8&redirect=true&ref_=as_li_tl&linkCode=ll1&tag=bigocheatsheet-1-20&linkId=2b0ec7f4eca859cce10f98824db5a73d)
- [High Performance JavaScript (Build Faster Web Application Interfaces)](https://www.amazon.com/Performance-JavaScript-Faster-Application-Interfaces/dp/059680279X/ref=as_li_ss_tl?ie=UTF8&redirect=true&ref_=as_li_tl&linkCode=ll1&tag=bigocheatsheet-1-20&linkId=fbbcd88ba96f0e3341687c8170e31cc2)

## Get the Official Big-O Cheat Sheet Poster

![img](http://bigocheatsheet.com/img/big-o-cheat-sheet-poster.png)

## Etc

[What's the best IDE for web development? See the results. Tell us what you think!](https://www.columm.com/eric/query/whats-the-best-ide-for-web-development)
