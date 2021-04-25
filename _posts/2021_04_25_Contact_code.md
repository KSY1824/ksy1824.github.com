---
layout: post
title: Contact code description
date: 2021-04-25
excerpt: "It doesn't seem to be good...."
tags: [class, code, HW]
comments: true
---

### code

~~~

class Contact:
    def __init__(self, name, phone_number, e_mail, addr):   # 겍체가 만들어질 때 인스턴스 변수 선언
        self.name = name
        self.phone_number = phone_number
        self.e_mail = e_mail
        self.addr = addr

    def print_info(self):   # print_contact로부터 호출 되었을때 주소록 프린트
        print("이름: ", self.name)
        print("폰번호: ", self.phone_number)
        print("이메일: ", self.e_mail)
        print("주소: ", self.addr)

def set_contact():
    name = input("이름: ")
    phone_number = input("폰번호: ")
    e_mail = input("이메일: ")
    addr = input("주소: ")
    contact = Contact(name, phone_number, e_mail, addr)
    return contact    # contact 변수 생성, 리턴

def print_contact(contact_list):
    for contact in contact_list:
        contact.print_info()    # print_info 호출

def delete_contact(contact_list, name):
    for i, contact in enumerate(contact_list):
        if contact.name == name:
            del contact_list[i]    # contact_list 내용 삭제

def load_contact(contact_list):
    f = open("address.txt", "rt")
    lines = f.readlines()
    num = len(lines) / 4
    num = int(num)    # 주소록 정보가 담긴 새 파일 생성

    for i in range(num):
        name = lines[4*i].rstrip('\n')
        phone = lines[4*i+1].rstrip('\n')
        email = lines[4*i+2].rstrip('\n')
        addr = lines[4*i+3].rstrip('\n')
        contact = Contact(name, phone, email, addr)
        contact_list.append(contact)    # contact_list 리스트에 주소록 정보 추가
    f.close()

def store_contact(contact_list):
    f = open("address.txt", "wt")
    for contact in contact_list:
        f.write(contact.name + '\n')
        f.write(contact.phone_number + '\n')
        f.write(contact.e_mail + '\n')
        f.write(contact.addr + '\n')
    f.close()

def print_menu():
    print("1. 연락처 입력")
    print("2. 연락처 출력")
    print("3. 연락처 삭제")
    print("4. 종료")
    menu = input("메뉴선택: ")
    return int(menu)

def run():
    contact_list = []
    load_contact(contact_list)  # load_contact 함수 호출
    while 1:
        menu = print_menu()
        if menu == 1:   # menu가 1일때
            contact = set_contact()    # set_contact 함수 호출
            contact_list.append(contact)    # contact_list에 contact 정보 추가
        elif menu == 2:   # menu가 2일때 print_contact 함수 호출
            print_contact(contact_list)
        elif menu == 3:   # menu가 3일때 delete_contact 함수 호출
            name = input("Name: ")
            delete_contact(contact_list, name)
        elif menu == 4:   # menu가 4일때 delete_contact 함수 호출, 프로그램 끝
            delete_contact(contact_list)
            break

if __name__ == "__main__":  # __name__ 변수가 "__main__" 일때 프로그램 시작 (run 함수 호출)
    run()
    
~~~

