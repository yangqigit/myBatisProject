# myBatisProject
mybatis工具类
创建一个mybatis工具类，在使用sql时很方便，不用大量维护xml文件
    QueryCondition<Net> cond = new QueryCondition<>();
    cond.setSelectFields("b.device_name,a.name");
    cond.from("wg_net a").leftJoin("pz_net_device b").on("a.device_id = b.id");
    cond.addWhereEx("net_id = "+netId);
    List<Net> netList = netMapper.queryByCond(cond);
