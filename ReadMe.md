![](images/logo.png)

### Calculating mean:

```c++
std::vector<int> v = {10, 40, 30, 50, 20};
mean<int> m;
std::cout << m.get_mean(v);
```

### Calculating weighted mean:

```c++
std::vector<float> vec = {1,2,3,4};
std::vector<float> weights = {1,2,3,4};
weighted_mean<float> wm;
float value = wm.get_weighted_mean(vec, weights);
```

### Calculating the median

```c++
std::vector<int> v = {10, 40, 30, 50, 20};
median<int> m;
std::cout << m.get_median(v);
```

### Calculating the mode

```c++
std::vector<int> v = {10, 40, 30, 50, 20};
mode<int> m;
std::cout << m.get_mode(v);
```

### Calculating the standard deviation

```c++
std::vector<double> v = {10, 40, 30, 50, 20};
standard_deviation<double> m;
std::cout << m.get_standard_deviation(v);
```

### Calculating the interquartile range

```c++
std::vector<float> v = { 6, 6 ,6, 6, 6.1, 8, 8, 8, 10, 10, 12, 12, 12, 12, 16, 16, 16, 16, 16, 20};
interquartile_range<float> m;
std::cout << m.get_interquartile_range(v);
```

Sometimes, your input for interquartile range shall have map with frequencies like this,
(Image source: HackerRank)
![](images/iqr.png)

You can convert this map to a vector using *frequency_converter* class.

**Example:**

```c++
std::map<float, unsigned long int> feq_map; // your frequency map
std::vector<float> v;  // The target vector where the result will be saved
frequency_map_converter<float> c;
c.to_vector(feq_map, v);
```

### Calculating the range:

```c++
std::vector<float> v = { 6, 6 ,6, 6, 6, 8, 8, 8, 10, 10, 12, 12, 12, 12, 16, 16, 16, 16, 16, 20};
range<float> m;
std::cout << m.get_range(v);
```

### Calculating the quartile:

```c++
std::vector<float> v = {7, 15, 36, 37.5, 39, 40, 41};
quartile<float> m;
std::map<std::string, float> result = m.get_quartile(v);
std::cout << "q1:\t" << result["q1"] << "\tq2:\t"<< result["q2"] << "\tq3:\t" << result["q3"];
```