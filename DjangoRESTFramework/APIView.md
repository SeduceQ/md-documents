# GET

```python
books = BookInfo.objects.all()
serializer = BookInfoModelSerializer(books, many=True)
return Response(serializer.data)
```

# POST

```python
book_dict = request.data
serializer = BookInfoModelSerializer(data=book_dict)
if serializer.is_valid():
    serializer.save()
    return Response(serializer.data)
else:
    return Response({"message": "保存失败"})
```

