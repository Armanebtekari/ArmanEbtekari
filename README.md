 Hi Im Arman Ebtekari:wave:
- I love making games and building sites:smiley:
- I want to be a web developer and game maker in the future:cowboy_hat_face:	
- my gmail armanebtekari@gmail.com:wink:
- Follow me🙏
<!--
**ArmanEbtekari/ArmanEbtekari** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.
use IgraalOSL\StatsTable\StatsTableBuilder;

create sp_UpdateStatistics
as
/*
	This procedure will run UPDATE STATISTICS against
	all user-defined tables within this database.
*/
declare 
	@tablename varchar(255),
	@tablename_header varchar(255)

declare tnames_cursor cursor for 
	select 
		'[' + ss.name + '].[' + so.name + ']'
	from 
		sys.objects so
		join sys.schemas ss on ss.schema_id = so.schema_id
	where 
		type = 'u'
	order 
		by ss.name, so.name

open tnames_cursor
fetch next from tnames_cursor into @tablename
while (@@fetch_status <> -1)
begin
	if (@@fetch_status <> -2)
	begin
		select @tablename_header = 'Updating ' + rtrim(upper(@tablename))
		print @tablename_header
		exec ('UPDATE STATISTICS ' + @tablename )
	end
	fetch next from tnames_cursor into @tablename
end
select @tablename_header = '****** NO MORE TABLES ******'
print @tablename_header

print 'Statistics have been updated for all tables.'
deallocate tnames_cursor
$statsTableBuilder->addIndexesAsColumn('date', 'Date');

$statsTable = $statsTableBuilder->build();

use IgraalOSL\StatsTable\Dumper\Excel\ExcelDumper;

$excelDumper = new ExcelDumper();
$excelContents = $excelDumper->dump($statsTable);

header('Content-type: application/vnd.ms-excel');
echo $excelContents


Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
