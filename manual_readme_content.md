[comment]: # " File: README.md"
[comment]: # "  Copyright (c) Mhike, 2022"
[comment]: # "  Licensed under the Apache License, Version 2.0 (the 'License');"
[comment]: # "  you may not use this file except in compliance with the License."
[comment]: # "  You may obtain a copy of the License at"
[comment]: # "    http://www.apache.org/licenses/LICENSE-2.0"
[comment]: # "  Unless required by applicable law or agreed to in writing, software distributed under"
[comment]: # "  the License is distributed on an 'AS IS' BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,"
[comment]: # "  either express or implied. See the License for the specific language governing permissions"
[comment]: # "  and limitations under the License."
[comment]: # ""
Fuse Box is designed to help deconflict events from within playbooks. By adding a "check fuse"
action to your playbook, you can pre-check whether you have handled this event before.  
Based on the identifying characteristics passed to the app, if the identifiers are duplicates of
previously checked content, it will "trip the fuse" and you can decide how to proceed based on that
information.  
This app should have a concurrency limit of 1 so that race conditions are avoided.  
The polling operation in Fuse Box manages retention in the list. If the polling action is not
scheduled, the retention limit in the configuration will not be respected
