create database exam;	--创建库

use exam;	--进库

create table Board(

	Board_ID int,
	
	Board_name char(20),
	
	Board_date datetime,
	
	Board_describe char(64)
	
	);
	
	insert Board values(11,'Board1',2016.12.24,'描述1');
	
	insert Board values(12,'Board2',2016.12.24,'描述2');
	
create table Forum(

	Forum_FID int,
	
	Forum_name char(20),
	
	Forum_describe char(64),
	
	Board_ID int
	
	);
	
	insert Board values(13,'Forum1','描述1'，11);
	
	insert Board values(14,'Forum2','描述1'，12);
	
create table moderator(

	Forum_FID int,
	
	User_UID int,
	
	operUID int,
	
	operDate date
	
	);

create table Article(

	Article_AID int,
	
	Article_theme char(32),
	
	Article_posttime datetime,
	
	Forum_FID int,
	
	Article_views int,
	
	Article_content char(255),
	
	Article_UID int,
	
	LastReplyDate datetime,
	
	LastReplyUID int
	
	);
	
create table Reply(

	reply_time datetime,
	
	reply_content char(255),
	
	reply_title char(128),
	
	reply_UID int,
	
	replydate datetime,
	
	Article_AID int
	
	);
	
create table User(

	User_UID int,
	
	UserName char(20),
	
	Password bigint
	
	);
	
create table UserDesc(		

	User_UID int,
	
	UserDesc_Desci varchar(20),
	
	UserDesc_Name varchar(20),
	
	UserDesc_Sex int,
	
	UserDesc_Birthday varchar(64)
	
	);
	
create table Entity7(

	User_UID int,
	
	RoleID int
	
	);
	
create table role(

	RoleID int,
	
	RoleName char(20)
	
	);
	
create table Entity9(

	Entity9_RID int,
	
	RoleID int
	
	);
	
create table RID(

	RightName char(20)
	
	);