# 3119009475-2
结对项目
以下则是我们expdao和userdao的代码：
Expdao：
package com.ood.mapper;

import com.ood.entity.ExpModel;

import java.util.List;


public interface ExpDao {
    void insertOne(ExpModel exp);

    List<ExpModel> selectByUserId(ExpModel exp);
}

Userdao：
package com.ood.mapper;

import com.ood.entity.UserModel;

public interface UserDao {

	UserModel selectOneByUserNameAndPwd(UserModel user);

	void insertOne(UserModel user);
}

还有些重要代码如：
Expmodel：
package com.ood.entity;


public class ExpModel {
    private int id;
    private int first;
    private int second;
    private int operate;
    private String result;
    private int userId;
    private String right;

    public ExpModel() {
    }

    public String getRight() {
        return right;
    }

    public void setRight(String right) {
        this.right = right;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public int getFirst() {
        return first;
    }

    public void setFirst(int first) {
        this.first = first;
    }

    public int getSecond() {
        return second;
    }

    public void setSecond(int second) {
        this.second = second;
    }

    public int getOperate() {
        return operate;
    }

    public void setOperate(int operate) {
        this.operate = operate;
    }

    public String getResult() {
        return result;
    }

    public void setResult(String result) {
        this.result = result;
    }

    public int getUserId() {
        return userId;
    }

    public void setUserId(int userId) {
        this.userId = userId;
    }
}

Usermodel;
package com.ood.entity;


public class UserModel {
    private int id;
    private String userName;
    private String userPwd;

    public UserModel() {
    }

    public UserModel(int id, String userName, String userPwd) {
        this.id = id;
        this.userName = userName;
        this.userPwd = userPwd;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getUserName() {
        return userName;
    }

    public void setUserName(String userName) {
        this.userName = userName;
    }

    public String getUserPwd() {
        return userPwd;
    }

    public void setUserPwd(String userPwd) {
        this.userPwd = userPwd;
    }
}
