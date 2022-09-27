# talksatconfs-data

This repository contains all the data on [talksatconfs.com](https://talksatconfs.com).

The data structured on website & this repository is constructed along following entities.
1. Conference
2. Event
3. Talk
4. Speaker
5. Video

```
Conference -> hasMany -> Events
Event -> hasMany -> Talks
Talk -> hasMany Speakers
Talk -> has -> Video
```

The data is stored in `YAML` format for the ease to edit the files when needed.

Each `conference` has its own folder in the `data/conferences` folder.

Each `conference` has a `_meta.yml` having basic information about the `conference`.

Eg:
```yml
name: AgentConf
description: ''
website: 'https://agent.sh'
twitter: agentconf
channel: 'youtube:UCYQweOJvW7EWa3_v7NdW-Gg'
tags: ''
```

The `events` that took every year or bi-yearly under that `conference` has its own file. The name of the file is the slug version of `Conference Name + Year`. Eg: `agentconf-2018.yml`

### Speakers
Speakers master data is maintained in the `speakers.yaml` file in the `data` folder.

We are thinking of a way to better manage the speakers data, since the file is growing too huge (currently 40,425 number of lines).

### Roadmap
[ ] adding validation while merging the new merge request & add it as a github action

[ ] adding tags to the talks entity for better contextual identification

[ ] also add more items in the roadmap, so that it becomes more clear and easy for other contributors to contribute & manage
