---
layout: post
title: "Link List(线性表的链式表示)"
date: 2015-09-02
categories: DataStructure
tags: DataStructure, LinkList
---

线性表的链式存储又称为单链表, |data|next|

单链表节点类型描述如下:

	typedef struct LNode{
		ElemType data;
		struct LNode *next;
	}LNode, *LinkList

####单链表基本操作的实现
#####1，采用头插法建立单链表

从一个空表开始,生成一个新节点，并将读取到的数据存放到新节点的数据域中,然后将新节点插入到当前链表的表头,即头节点之后。

	LinkList CreateList1(LinkList &L){
		LNode *s; int x;
		L=(LinkList)malloc(sizeof(LNode));
		L->next=NULL;
		scanf("%d",&x);
		while(x!=9999){
			s=(LNode8)malloc(sizeof(LNode));
			s->data=x;
			s->next=L->next;
			L->next=s;;
			scanf("%d", &x);
		}
		return L;
	}