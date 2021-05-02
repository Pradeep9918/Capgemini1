# Capgemini1
package com.springcore.bean.javabased.configuration;

import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;

import com.springcore.bean.javabased.StudentBean;

@Configuration
public class StudentBeanConfiguration {

	@Bean(name="student")
	public StudentBean getStudent() {
		// you can use any constructor 
		StudentBean s = new StudentBean();
		s.setStudentId(1234);
		s.setStudentName("stud1");
		s.setAge(23);
		//remaining properties setting  other wise null values will be inserted
		return s;
	}
}
