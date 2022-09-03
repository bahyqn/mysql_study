### create table
    DROP TABLE IF EXISTS books;  
    CREATE TABLE books(  
        id INT PRIMARY KEY AUTO_INCREMENT,  
        isbn CHAR(20) NOT NULL COMMENT 'isbn号',  
        book_name VARCHAR(120) NOT NULL COMMENT '书名',  
        auther VARCHAR(60) NOT NULL COMMENT '作者',  
        press VARCHAR(60) NOT NULL COMMENT '出版社',  
        publication_date DATE NOT NULL COMMENT '出版日期',  
        price DECIMAL(9, 2) COMMENT '价格'  
    )ENGINE=INNODB DEFAULT CHARSET=utf8;

    INSERT INTO books(isbn, book_name, auther, press, publication_date, price) VALUES
    ('978-7-302-14751-0', '数据结构', '严蔚敏', '清华大学出版社', '2020-01-01', 39.00),
    ('978-7-04-022390-3', '计算机组成原理', '唐朔飞', '高等教育出版社', '2020-01-01', 45.00);

    SELECT * FROM books;

    # delete column
    ALTER TABLE books DROP price;

    # add column
    ALTER TABLE books ADD COLUMN column_name column_type;
    ALTER TABLE books ADD COLUMN new_price DECIMAL(9, 2);

    # change column name and type
    ALTER TABLE books CHANGE old_column new_column DECIMAL(8, 2);
    ALTER TABLE books CHANGE new_price old_price DECIMAL(8, 2);

    # change column type
    ALTER TABLE books MODIFY column_name column_type;
    ALTER TABLE books MODIFY old_price INT;

### less use
    ALTER TABLE 表名 ENGINE=新的存储引擎类型
    ALTER TABLE 表名 DEFAULT CHARSET=新的字符集
    ALTER TABLE 表名 AUTO_INCREMENT=新的初始值
    ALTER TABLE 表名 PACK_KEYS=新的压缩类型 
    
    ALTER TABLE books ENGINE=MYISAM;
    ALTER TABLE books DEFAULT CHARSET=gb2312;