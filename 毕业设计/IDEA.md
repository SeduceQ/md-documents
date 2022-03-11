# 模糊查询

> 在相应的filter里编写
>
> ```python
> class Filter(django_filters.rest_framework.FilterSet):
>     字段名 = django_filters.CharFilter(lookup_expr='icontains')
> 
>     class Meta:
>         model = BranchInfo
>         fields = ["branch_name"]
> ```
>
> `lookup_expr`使用`icontains`表示忽略大小写的模糊查询
>
> `fields`表示在哪些字段里进行查询

# 