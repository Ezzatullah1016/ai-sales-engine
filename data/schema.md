# Lead Data Schema

Use these columns in every raw and scored lead file so the agents read them
consistently. Raw files can be messy or missing columns — the lead-scorer
agent maps whatever it finds into this shape.

| Column        | Meaning                                                        |
|---------------|----------------------------------------------------------------|
| source        | bark / upwork / facebook / instagram / scrape / referral       |
| capture_date  | YYYY-MM-DD                                                      |
| company       | organisation name                                              |
| contact_name  | person, if known                                               |
| role          | their job title, if known                                      |
| email         | only if legitimately obtained; never guessed                   |
| phone         | optional                                                       |
| website       | full URL                                                       |
| country       | target market                                                  |
| channel       | the channel you intend to use for outreach                     |
| raw_need      | what they asked for, or the Upwork/Bark post text              |
| score         | 0-100 (filled by the lead-scorer agent)                        |
| score_reason  | one line on why                                                |
| status        | new / researching / contacted / replied / proposal / won / lost|
| owner         | salesperson assigned                                           |
| last_touch    | YYYY-MM-DD                                                      |
| next_step     | the next action                                                |
| notes         | free text                                                      |
