# lua-json-base64
Lua json_encode,json_decode,base64_encode,base64_decode



# How to use

Example:

array = {}

array["k"] = "v"
array["ar"] = {}
array["ar"]["k"] = "v"

dvt = json_encode(array)

print(dvt)

Results: {"k":"v","ar":{"k":"v"})


print(json_decode(dvt))


Results:

{
k = "v",
ar = {
k = "v"
}
}
