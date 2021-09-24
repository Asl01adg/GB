# GB
USE vk;
SELECT * FROM messages;
 
-- рондомный пользователь - 55.

SELECT id, from_user_id, to_user_id, is_important FROM messages WHERE to_user_id = 55;

-- 55 пишет только 16 поьзователь
 
UPDATE  messages SET to_user_id = 16, from_user_id = 55, is_important = 1, body = 'any some text' WHERE id = 72;
INSERT INTO messages SET to_user_id = 16, from_user_id = 55, is_important = 1, body = 'some text';

SELECT from_user_id, to_user_id, is_important FROM messages WHERE from_user_id = 16;

-- 16 пользователь пишет 55, 11, 80

SELECT from_user_id, to_user_id, is_important FROM messages WHERE from_user_id = 16 AND is_important = 1; 

-- но если учитывать важность диалогов, то 55, в приоритете.

SELECT * FROM likes;



SELECT gender, count(*) AS cnt FROM users GROUP BY gender;

-- так как лайки упорядоченны, не зна. почему так, следую предположить по этому выводуБ что лайки женщин больше.

SELECT * FROM posts;

-- это тестовый вариант чтоб понять что я разобрался с гитом
