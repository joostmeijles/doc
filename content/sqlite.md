---
title: Sqlite
menu: main
---

- `sq3dh` SqLite console
- `sqlgui` SpatiaLite gui
- `select * from dh_metadata LIMIT 2;` Show DHive Metadata
- `.schema dh_metadata`
- `update dh_metadata set MetaValue = 2.264 where MetaTag = 'DH_VERSION';` Set DHive version
- `.exit`
- `select * from dh_mde where EnumGroup = "VIMP";` Select enums from VIMP (Vehicles impacted group), see DHive_Model/h_dh.h
- `.header on`
- `attach "./deu_msp_vw_its_ts_20150218.dh.sq3" as ref;`
- `select * from sfm_speedlimit_matches sign, dh_sms sms, dh_ssa ssa where sign.sms_id=sms.id and sms.id=ssa.smsid and ssa.attributename=201 and ssa.attributevalue=209;`
- `select SMSId  from ref.dh_ssa where AttributeName = 201 AND AttributeValue = 209;` Select SMS ids for attribute H_DH_SSA_NAME_SIGN_CONSTRAINT with value H_DH_SSA_VALUE_SIGN_CONSTRAINT_WHEN_WET
