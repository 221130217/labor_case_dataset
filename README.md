# Labor Disputes Dataset

## Source
- The data are retrieved from China Judgment Online (裁判文书网）
- All cases are under the primary category Labor and Personnel Dsiputes (劳动、人事争议）
- The time range is from 2021-10 to 2024-11

## Summary
|  Year  | Month Range  | Records |
|  ----  | ----  | ----  |
| 2024  | 01 - 11 | 6,492 |
| 2023  | 01 - 12 | 32,332 |
| 2023  | 01 - 12 | 77,412 |
| 2023  | 10 - 12 | 30,331 |
| **Sum** |       | **146,567** |


## Description
### 1. content
The files in the content folder are the original text content retrieved from China Judgment Online. We append an unique identifier to each case. The identifier is composed by CASE_NUMBER|CASE_TITLE|JUDGMENT_DATE


### 2. json
The files in the json folder contains the metadata and the extracted fact & judgment elements. An example is shown below.

```
{
  'original_data':
    {
      'identifier': '（2024）陕0526民初342号|王文军与中国铁路西安局集团有限公司韩城车务段劳动争议一审民事判决书|2024-05-07',
      'caseNumber': '（2024）陕0526民初342号',
      'caseType': '民事案件',
      'court': '蒲城县人民法院',
      'judgementDate': '2024-05-07',
      'publishDate': '2024-06-15',
      'reason': '劳动争议',
      'title': '王文军与中国铁路西安局集团有限公司韩城车务段劳动争议一审民事判决书'
    },
  'qwen_res':
  {
    'proponents': [
      {'name': '王文军', 'type': '自然人', 'role': '申请人', 'affiliation': '中国铁路西安局集团有限公司韩城车务段钟家车站'},
      {'name': '关树斌', 'type': '自然人', 'role': '委托代理人', 'affiliation': '陕西康秦律师事务所律师'}
    ],
    'opponents': [
      {'name': '中国铁路西安局集团有限公司韩城车务段', 'type': '公司', 'role': '被申请人', 'affiliation': '有限责任公司分公司（非自然人投资或控股的法人独资）'},
      {'name': '危小珂', 'type': '自然人', 'role': '法定代表人', 'affiliation': '中国铁路西安局集团有限公司韩城车务段'},
      {'name': '周曙光', 'type': '自然人', 'role': '委托代理人', 'affiliation': '陕西丰瑞（西咸新区）律师事务所律师'},
      {'name': '王瑞芳', 'type': '自然人', 'role': '委托代理人', 'affiliation': '中国铁路西安局集团有限公司韩城车务段'}
    ],
    'judges': [{'name': '同小虎', 'type': '审判员'}],
    'proponentArguments': ['判决被告继续履行与原告之间的劳动合同', '诉讼用由被告承担'],
    'opponentArguments': ['被告解除与原告的劳动合同关系，符合《劳动合同书》约定及法律规定，程序合法，解除行为合法有效', '原告要求继续履行劳动合同没有法律依据，依法应当驳回', '原告在起诉状中称，《关于解除王文军同志劳动合同的通知》表述的劳动合同签订时间及编号与劳动仲裁中被告提交的劳动合同不符，影响了原告“劳动仲裁抗辩权的行使”。原告该项陈述没有任何法律依据，依法不应采信', '原告称解除已经超过法定期限，没有事实与法律依据，依法应当驳回', '根据法庭调查得知，原、被告间仅有一份书面合同，双方对合同的适用与内容不存在分歧，原告对被告提供的合同的真实性以及劳动合同管理实施办法真实性均予以认可，合同及实施办法对于吸食毒品被强制隔离戒毒均有明确规定，所以本案被告解除合同是有制度和事实依据的'],
    'factElements': {
    'entryDate': '1998年12月',
    'officialContract': '是',
    'latestContract': {'from': '2014年1月1日', 'to': '法定终止情形出现时止', 'type': '无固定期限合同'},
    'position': [{'name': '铁路车站业务', 'byContract': '是', 'actual': '是', 'indoor': 'unknown'}],
    'monthlySalary': {'byContract': 'unknown', 'actual': 'unknown', 'distributeMethod': 'unknown', 'average12Month': 'unknown'},
    'socialInsurance': {'payment': 'unknown', 'from': 'unknown', 'to': 'unknown', 'compensation': 'unknown', 'compensationAmount': 'unknown', 'compensationType': 'unknown'},
    'currentStatus': {'resign': '否', 'resignDate': 'unknown', 'resignReason': 'unknown', 'officialNotice': '是', 'officialNoticeType': '解除', 'officialNoticeDate': '2023年8月31日', 'handover': 'unknown', 'handoverDate': 'unknown'},
    'laborRelation': '是',
    'overtime': '否',
    'annualLeave': '否',
    'workInjuryBenifits': '否',
    'medicalPeriodBenifits': '否',
    'nonCompetition': '否'
  },
  'lawArticles': [{'code': '《中华人民共和国劳动法》', 'section': '第二条'}, {'code': '《中华人民共和国劳动法》', 'section': '第十六条'}, {'code': '《中华人民共和国劳动法》', 'section': '第十七条'}, {'code': '《中华人民共和国劳动合同法》', 'section': '第三十九条'}],
  'judgement': ['驳回原告王文军的诉讼请求', '案件受理费10元，减半收取5元，由原告王文军负担', '如不服本判决，可在判决书送达之日起十五日内，向本院递交上诉状，并按对方当事人的人数提出副本，上诉于陕西省渭南市中级人民法院']},
  'region': '陕西省渭南市蒲城县'
}

```
