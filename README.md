# SimpleSpringSecurity

ReadMe:

ReadMe:
Spring Security Simple  [name : simpleSpringSecurity]

Get : /allUser  —> returns ——> list of all user
Get: /User/{userId} —> returns ——> specified user
POST :  /User/addUser —> returns ——> add user into the database



So, after creating simple CURD User, now we need to add the spring security dependency along with test dependency as well

<dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-security</artifactId>
    </dependency>

<dependency>
      <groupId>org.springframework.security</groupId>
      <artifactId>spring-security-test</artifactId>
      <scope>test</scope>
    </dependency>

Now, need to stop the server and start again, than we will see the login page and password will appears in log console and username is : user

Now, open postman and configure authentication  






So this above work flow for the authentication on the postman,

Now, in eclipse , crate the config folder and create the MyConfigSecurity class

After creating
 protected void configure(HttpSecurity http) throws Exception {
		http
				.authorizeRequests()
				.anyRequest()
				.authenticated()
				.and()
				.httpBasic();
				

	}

Refresh the application, and login page will change




