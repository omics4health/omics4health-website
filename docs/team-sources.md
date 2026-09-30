# Team profile sources

Checked on 2026-09-30. Members are displayed alphabetically by surname (`last_name`), as requested by the organizer. Research descriptions are brief paraphrases; the university profile links on Team provide the full source. The previous Wubing Zhang entry is no longer displayed; its source files remain untouched.

| Member | Profile source | Verification |
| --- | --- | --- |
| Xiaotao Shen | https://dr.ntu.edu.sg/entities/person/Xiaotao-Shen | Page HTML and embedded Person metadata; Nanyang Assistant Professor, Lee Kong Chian School of Medicine, NTU. |
| Qi Su | https://www.mect.cuhk.edu.hk/people/qisu.html | Page loads https://www.mect.cuhk.edu.hk/people/qisu.json; verified name, title, affiliation, interests and portrait there. |
| Na Jiao | https://life.fudan.edu.cn/0f/e9/c31282a659433/page.htm | Official bilingual profile; title retained as 青年研究员 instead of inventing an equivalent academic rank. |
| Ye Peng | https://sphpc.cuhk.edu.hk/yepeng/ | Direct page and staff-directory requests timed out. Text verified through the search index of this exact university page, and corroborated by the CUHK research directory. Portrait remains unavailable; initials are a placeholder. |
| Chang Liu | https://www.mbtechinst.qd.sdu.edu.cn/info/1087/8030.htm | Official profile states Professor since January 2025; research interests are gut microbial culturomics and functional gut bacteria. |
| Xin Zhou | https://imi.fudan.edu.cn/info/1525/1148.htm | Official profile; title retained as 青年研究员. Institute name is translated from 复旦大学智能医学研究院. |

Ye Peng corroborating directory: https://research.cuhk.edu.hk/en/organisations/the-jockey-club-school-of-public-health-and-primary-care/persons/

Ye Peng's displayed profile link was changed to the user-provided https://www.linkedin.com/in/ye-peng-68231a110/ on 2026-09-30. LinkedIn redirects to a login/sign-up wall; the public search index only corroborates the CUHK school affiliation. His existing title, biography and initials placeholder are retained pending accessible profile content or a user-provided update; these fields have not been reverified against LinkedIn.

## Portrait provenance

Images are the original public university assets, stored in `static/images/team/`; display cropping is CSS only.

- Xiaotao Shen: https://dr.ntu.edu.sg/bitstreams/9640c488-3def-4a0b-be62-981c4815f101/download
- Qi Su: https://www.mect.cuhk.edu.hk/images/people/qisu.png
- Na Jiao: https://life.fudan.edu.cn/_upload/article/images/a1/ab/42688f4643479204c23730a20ccd/41358285-5540-42fa-811e-84b4bdf5568b.jpg
- Chang Liu: https://www.mbtechinst.qd.sdu.edu.cn/__local/F/E7/98/49C70146EA5236F31741EA1D7FA_0DA0209A_884FD.jpg
- Xin Zhou: the `virtual_attach_file.vsb` portrait URL embedded in the official profile (the profile is the stable source link).

To replace Ye Peng's placeholder, add a verified portrait and set `image: images/team/ye-peng.jpg` in `data/organizers.yaml`.

## Additional organizers (2026-09-30)

- Jiliang Hu: https://smart.org.cn/smart-fellow/hujiliang ; affiliation and department corroborated at https://en.szbl.ac.cn/research/groups/Jiliang-Hu.htm . The English SMART Fellow directory uses Junior Principal Investigator: https://smart.org.cn/en/smart-fellow?index=&page=4&subject=&unit= . Portrait comes from the supplied SMART profile.
- Zhiyuan Li: https://cqb.pku.edu.cn/info/1002/1817.htm . Role (Assistant Professor), department, research description and portrait follow the supplied university profile.
- Shengbo Wu: https://eng.ox.ac.uk/people/shengbo-wu . Oxford's official visitor profile explicitly identifies him as Associate Professor at Zhejiang Institute of Tianjin University, Shaoxing; used for role, research and portrait. The affiliation is Tianjin University, not Oxford.

Contact was changed to `omics4health@gmail.com` at the user's request as a placeholder only; no mailbox was created or verified.
