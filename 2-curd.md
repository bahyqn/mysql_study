### create table
DROP TABLE IF EXISTS books;
CREATE TABLE books(
    id INT PRIMARY KEY auto_increment,
    isbn CHAR(13) NOT NULL COMMENT 'isbn号',
    book_name VARCHAR(120) NOT NULL COMMENT '书名',
    auther VARCHAR(60) NOT NULL COMMENT '作者',
    press VARCHAR(60) NOT NULL COMMENT '出版社',
    publication_date DATE NOT NULL COMMENT '出版日期',
    price DECIMAL(9, 2) COMMENT '价格'
)ENGINE=INNODB DEFAULT CHARSET=utf8;

