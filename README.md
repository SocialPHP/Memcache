# Memcache



//Connect to memcache

$memcache = new Memcache();
$memcache->addServer('127.0.0.1', 11211);



//Add data

$memcache->set('user_last_visit_'.$user_info['user_id'], $server_time, (3600*24*3));



//Data output

$memcache->get('user_last_visit_'.$user_info['user_id'], $server_time, (3600*24*3));



//Data delete

$memcache->delete('user_last_visit_'.$user_info['user_id'], $server_time, (3600*24*3));



