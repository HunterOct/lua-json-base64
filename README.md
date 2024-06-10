# lua-json-base64
Lua library for use base64 and json

# How to use

local HTFUNC;

--GameGuardian gửi yêu cầu truy cập

local API = gg.makeRequest("https://raw.githubusercontent.com/HunterOct/lua-json-base64/main/json-base64.lua").content

--Kiểm tra nếu bạn đã cấp quyền truy cập. nếu đúng thì nó sẽ tiến hành tải mã bên trong link truy cập và chạy nó

if API then

    HTFUNC = load(API)();
  
else

    --Nếu không thì thông báo lỗi và thoát
    gg["alert"]("Lỗi Bạn chưa cấp quyền truy cập internet!")
  
    os.exit()
  
end

local t = {};

t["abc"] = "xyz";
t["VietNam"] = "Number One";

print(HTFUNC["base64"]["decode"](HTFUNC["base64"]["encode"]("abc")));


print(HTFUNC["json"]["decode"](HTFUNC["json"]["encode"](t)));
