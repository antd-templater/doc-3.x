```typescript [-> Mock 数据]
import { promiser, resolver, worker, rester } from "@/mock/setup";
import { http, HttpResponse } from "msw";

const tag = "获取用户信息";
const url = resolver("/auth/loginUserInfo");

worker.use(
  http.post(url, async req => {
    const body = await rester.body(req);
    const query = await rester.query(req);
    const params = await rester.params(req);
    const printer = await rester.printer(tag);

    const resource = {
      code: "0000",
      message: null,
      result: {
        userNo: "182588xxx88",
        userName: "admin",
        mobilePhone: "182588xxx88",
        postName: "系统管理",
        orgId: "101.100.131",
        orgName: "北仑网安通信有限公司",
        deptId: "1126534161135795132",
        deptName: "软件部",
        dataFlag: "2",
        activity: "Y",
        role: {
          permissions: [
            {
              permissionId: "ResourceManage", // 资源管理页面
              actionEntitySet: [
                { action: "add", defaultCheck: false, describe: "新增" },
                { action: "del", defaultCheck: false, describe: "删除" }
              ]
            },
            {
              permissionId: "RoleManage", // 角色管理页面
              actionEntitySet: [
                { action: "add", defaultCheck: false, describe: "新增" },
                { action: "del", defaultCheck: false, describe: "删除" },
                { action: "edit", defaultCheck: false, describe: "修改" },
                { action: "query", defaultCheck: false, describe: "查询" }
              ]
            },
            {
              permissionId: "OrganizeManage", // 组织管理页面
              actionEntitySet: [
                { action: "add", defaultCheck: false, describe: "新增" },
                { action: "del", defaultCheck: false, describe: "删除" },
                { action: "edit", defaultCheck: false, describe: "修改" },
                { action: "query", defaultCheck: false, describe: "查询" }
              ]
            },
            {
              permissionId: "UserManage", // 用户管理页面
              actionEntitySet: [
                { action: "add", defaultCheck: false, describe: "新增" },
                { action: "del", defaultCheck: false, describe: "删除" },
                { action: "edit", defaultCheck: false, describe: "修改" },
                { action: "query", defaultCheck: false, describe: "查询" }
              ]
            }
          ]
        }
      }
    };

    // 打印日志 (浏览器端)
    printer(log => {
      log("[body] - ", body);
      log("[query] - ", query);
      log("[params] - ", params);
      log("[resource] - ", resource);
    });

    // 延时 0s, 即返回响应
    return promiser(HttpResponse.json(resource), 0);
  })
);
```
