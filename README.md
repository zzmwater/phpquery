# phpquery
php爬虫类


使用案例
   爬虫兔区实例
		header("Content-type: text/html; charset=utf-8");
		$o = new \phpQuery();
	
            $o->newDocumentFileHTML('http://bbs.jjwxc.net/board.php?board=2&page=1' ,$charset = 'utf-8');
            foreach (pq("#msglist tr[valign='middle']") as $ui=>$li) {
                $lb = trim(pq($li)->find("td:eq(0)")->text());
				$href = pq($li)->find("td:eq(2)")->find("a:eq(0)")->attr('href');
				$zt = trim(pq($li)->find("td:eq(2)")->text());
                $zz = trim(pq($li)->find("td:eq(4)")->text());
                $ftsj = trim(pq($li)->find("td:eq(5)")->text());
                $hf = trim(pq($li)->find("td:eq(6)")->text());
                $hfsj = trim(pq($li)->find("td:eq(7)")->text());
		     var_dump($lb);die;
				}
		
		