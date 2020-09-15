---
title: Expressive code with STL
date: 2020-08-17
layout: post
navigation: True
comments: false
class: post-template
toc: true
image: assets/images/move.jpg
categories: [C++11, STL]
author: Anurag
---

https://leetcode.com/problems/running-sum-of-1d-array/
```cpp

vector<int> runningSum1(vector<int>& nums) 
{
    vector<int> ans;   
    long sum = 0;

    for(auto& a : nums )
    {
        sum += a;
        ans.emplace_back(sum);
    }
    
    return ans;
}
```

```cpp
vector<int> runningSum2(vector<int>& nums) {
    partial_sum(nums.begin(), nums.end(), nums.begin());
        
    return nums;
}
```

```cpp
make_heap
push_heap
pop_heap
sort_heap

sort
partial_sort
n_th element - similar to quick sort pivot.

inplace_merge

partition

rotate
shuffle
next_permutation
prev_permutation
reverse

stable_sort
stable_partition

is_sorted
is_partitioned
is_heap

is_sorted_until
is_partitioned_until
is_heap_until

count
accumulate/reduce/transform_reduce
partial_sum
(transform_)inclusive_scan
(transform_)exclusive_sum
inner_product
adjacent_difference
sample

all_of - true with empty collection
any_of - false for empty collection
none_of - true for empty collection

equal
is_permutation
lexicographical_compare
mismatch - stop at first poition of difference.     returns pair of iterators.

find
adjacent_find
equal_range
lower_bound
upper_bound
binary_search

search - searches a subrange in a range
find_end - searches subrange in range from end
find_first_of

max_element
min_element
min_max_element

set_difference
set_intersection
set_union
set_symmetric_difference
includes
merge

copy
move - calls std::move on all the elements
swap_ranges
copy_backwards
move_backwards

fill
generate
iota
replace

remove - instead use erase on container
unique - removes adjacent duplicaes 

//leave the input collection untouched
remove_copy
unique_copy
reverse_copy
rotate_copy
replace_copy
partition_copy
partial_sort_copy


find_if
find_if_not
count_if
remove_if
remove_copy_if
replace_if
replace_copy_if
copy_if

transform - two overloads

for_each -  read up about side effect

uninitialized_fill
uninitialized_copy
uninitialized_move
destroy
uninitialized_default_constructor
uninitialized_value_constructor

copy_n
fill_n
generate_n
search_n
for_each_n
uninitialized_copy_n
uninitialized_fill_n
uninitialized_move_n
uninitialized_default_constructor_n
uninitialized_value_constructor_n
destroy_n

```