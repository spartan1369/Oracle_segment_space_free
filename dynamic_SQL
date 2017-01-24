DECLARE
load_owner varchar2(300):=USER;
load_tablename varchar2(300):='OBJ$';
load_type varchar2(300):='TABLE';
load_fs1_bytes NUMBER ;
load_fs2_bytes NUMBER ;
load_fs3_bytes NUMBER ;
load_fs4_bytes NUMBER ;
load_fs1_blocks NUMBER ;
load_fs2_blocks NUMBER ;
load_fs3_blocks NUMBER ;
load_fs4_blocks NUMBER ;
load_full_bytes NUMBER ;
load_full_blocks NUMBER ;
load_unformatted_bytes NUMBER;
load_unformatted_blocks NUMBER;
BEGIN
	dbms_space.space_usage(
	segment_owner=> load_owner ,
	segment_name=>  load_tablename ,
	segment_type=>upper(load_type),
	fs1_bytes=>load_fs1_bytes,
	fs1_blocks=>load_fs1_blocks,
	fs2_bytes=>load_fs2_bytes,
	fs2_blocks=>load_fs2_blocks,
	fs3_bytes=>load_fs3_bytes,
	fs3_blocks=>load_fs3_blocks,
	fs4_bytes=>load_fs4_bytes,
	fs4_blocks=>load_fs4_blocks,
	full_bytes=>load_full_bytes,
	full_blocks=>load_full_blocks,
	unformatted_bytes=>load_unformatted_bytes,
	unformatted_blocks=>load_unformatted_blocks 
	);
	dbms_output.put_line('user = '||load_owner||'         SEGMENT NAME ='||load_tablename);
	dbms_output.put_line('0-25%   Free blocks = '||load_fs1_blocks||'         Bytes ='||load_fs1_bytes);
	dbms_output.put_line('25-50%  Free blocks = '||load_fs2_blocks||'         Bytes ='||load_fs2_bytes);
	dbms_output.put_line('50-75%  Free blocks = '||load_fs3_blocks||'         Bytes ='||load_fs3_bytes);
	dbms_output.put_line('75-100% Free blocks = '||load_fs4_blocks||'        Bytes ='||load_fs4_bytes);
	dbms_output.put_line('Full    Free blocks = '||load_unformatted_blocks||'         Bytes ='||load_unformatted_bytes);
END ;
