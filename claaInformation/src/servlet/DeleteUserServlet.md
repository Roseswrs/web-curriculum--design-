```java
/*
author:14130140358 赵妍
*/
package com.yzz.web.servlet;

import java.io.IOException;

import javax.servlet.ServletException;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;

import com.yzz.domain.User;
import com.yzz.service.UserService;

public class ChangeInfo extends HttpServlet {

	public void doPost(HttpServletRequest request, HttpServletResponse response)
			throws ServletException, IOException {
		request.setCharacterEncoding("utf-8");
		response.setContentType("text/html;charset=utf-8");
		
		// 获取表单数据并保存到bean中
				User form = new User();
				String username = request.getParameter("username");
				String password = request.getParameter("password");
				String gender=request.getParameter("gender");
				String stuId = request.getParameter("stuId");
				
				
				form.setUsername(username);
				form.setPassword(password);
				form.setStuId(stuId);
				form.setGender(gender);
				
				
				UserService service=new UserService();
				service.changeInfo(form);
				
				
				request.getSession().setAttribute("user",form);
				
				response.sendRedirect("user/userInfo.jsp");
	}

}


