I.小组使用的工具与具体合作方式 
The tools and the specific cooperation methods we used 
·会议（线下 + 线上）：线下利用课后时间面对面讨论，效率更高，且能灵活补充线	上会议的不足。线上以腾讯会议为主，每周至少进行一次全组会议，同步整体进度	和方向；模块相关的具体问题则由相关组员随时按需召开（Specific issues related to 	the module will be addressed by the relevant team members at anytime as needed）。
·看板与想法记录（Notion）：用于任务分配、进度追踪和新想法的汇集。任何关		于游戏设计或架构的新思路随时记录，方便全员查看讨论，不让好想法在聊天		记录里消失。
·日常沟通（Wechat Group）：信息传达最快的渠道。每次Notion有任务更新时同步	在群里说明，遇到阻碍或紧急问题第一时间在群里提出。
·版本控制（GitHub）：所有代码提交和版本发布的唯一平台。
·其他工具：类图工具（Lucidchart）
画图工具（Procreate）
打分工具（Planning Poker，用于Estimate user stories）
投票软件（Online anonymous questionnaire）
框架基石（P5.JS，是学习JavaScript的引导，提供基础代码框架）
并行开发（Git Branching，用于将分支代码合并到主库中）

[![WeChat](https://img.shields.io/badge/WeChat-微信群-07C160?style=flat&logo=wechat&logoColor=white)](https://weixin.qq.com)

[![Notion](https://img.shields.io/badge/Notion-任务看板-000000?style=flat&logo=notion&logoColor=white)](https://notion.so)

[![GitHub](https://img.shields.io/badge/GitHub-版本控制-24292e?style=flat&logo=github&logoColor=white)](https://github.com)

[![Next.js](https://img.shields.io/badge/Next.js-16.2.4-000000?style=flat&logo=next.js&logoColor=white)](https://nextjs.org)

[![p5.js](https://img.shields.io/badge/p5.js-框架基石-ED225D?style=flat&logo=p5.js&logoColor=white)](https://p5js.org)

[![Lucidchart](https://img.shields.io/badge/Lucidchart-类图工具-FF6B00?style=flat)](https://lucidchart.com)

[![Planning Poker](https://img.shields.io/badge/Planning_Poker-故事点估算-5B4FBE?style=flat)](https://planningpokeronline.com)



[![My Skills](https://skillicons.dev/icons?i=nextjs,github,npm,notion,figma)](https://skillicons.dev)


## I. 小组使用的工具与具体合作方式

### 会议 ![](https://skillicons.dev/icons?i=notion&theme=light&perline=1) 
线下利用课后时间面对面讨论...

### 版本控制 [![](https://skillicons.dev/icons?i=github)](https://github.com)
所有代码提交和版本发布的唯一平台。


## I. 小组使用的工具与具体合作方式

![](https://skillicons.dev/icons?i=github,npm,figma,notion)
\


## Project Structure

```
costume-stock-app/
├── __tests__/                               # Test files (API and frontend)
│   ├── api/                                 # Backend API tests
│   └── browser/                             # Frontend component tests
├── src/
│   ├── app/                                 # Next.js App Router
│   │   ├── admin/                           # Admin dashboard
│   │   │   ├── layout.tsx                  
│   │   │   ├── Sidebar.tsx                   
│   │   │   ├── bookings/                    # Booking management
│   │   │   ├── users/                       # User management
│   │   │   └── stock/                       # Costume inventory
│   │   ├── api/                             # Backend API routes
│   │   │   ├── costume/                     # Costume endpoints
│   │   │   ├── images/                      # Image endpoints
│   │   │   └── s3/                          # S3 upload endpoints
│   │   ├── costume/                         # Costume catalog
│   │   ├── login/                             
│   │   ├── layout.tsx                         
│   │   └── page.tsx                         # Homepage
│   ├── components/                          # Reusable UI components
│   │   ├── admin/                              
│   │   ├── filter/                            
│   │   ├── form/                             
│   │   ├── pagination/                     
│   │   ├── ui/                              # Generic UI (Button, NavBar)
│   │   └── user-management/                 
│   └── lib/                                 # Utilities and configs
│       ├── auth/                            # Authentication logic
│       ├── prisma.ts                        # Database client
│       ├── s3/                           
│       └── utils.ts                       
├── public/                                  # Static assets
├── docs/                                    # Documentation
└── configuration files                      # next.config.js, package.json, tsconfig.json
```

## Stakeholders

### Bookers (direct) - Drama students/Society members
- **Description**: The primary users of the platform, who need to find and book costumes for rehearsals and performances.  
- **Pain points**: Borrowers are unable to view costume information after closing the costume room, and cannot confirm size or upper body effect, often wasting time commuting between costumes.
- **Goal**: Quickly find suitable costumes, remotely check availability, and reduce the risk of not being able to find costumes before performances.

### Admin (direct) - Staff of the theater department
- **Description**: The secondary users of the platform is responsible for managing the borrowing and returning records and inventory information of a large number of costumes to ensure the smooth borrowing process.
- **Pain points**: Manual registration of borrowing and returning records is prone to errors, and it is difficult to track the location of costumes in time. Excel or notebook management is prone to confusion in the performance season, resulting in low work efficiency due to repeated work.
- **Goal**: Effectively manage the borrowing and returning of costumes, know which costumes have been lent, returned or overdue in real time, and reduce repeated answers to the borrower's questions about inventory and size.

### Legislators (indirect) - UoB staff protecting & securing data
- **Goal**: Protect student personal data, ensure the traceability of borrowing behavior, meet audit requirements, and comply with GDPR/UK data protection regulations.

### Viewers (indirect) - UoB students/The public
- **Goal**: See higher quality visual effects when enjoying the performance.  

## User Stories

#### As a Booker

- **Story 1.** I want to be able to find and book costumes from anywhere at anytime, in order to save time because I don't need to go to where the costumes are stored.
- **Story 2.** I would like to see the actual wearing effect of the costume on a person, rather than guessing the size by hanging it on a hanger, so as to reduce the risk of borrowing the wrong size and avoid discovering the incompatibility before the performance.
- **Story 3.** I want to filter costumes like on an e-commerce platform (e.g., Victorian era, black, men’s, XL) so that I can accurately find what I need without having to search through the entire costume room.
- **Story 4.** I want to see in real time whether a costume has been borrowed so that I can avoid making a wasted trip and improve efficiency.

#### As a Admin

- **Story 1.** I want to use my phone to take photos of new costumes, fill in a small amount of information, and upload them, so that even people with non-technical backgrounds can maintain the system.
- **Story 2.** I want to be able to quickly see at a glance which costumes need to be returned today, who hasn't returned them, and how long they are overdue, so as to replace manually flipping through a notebook and improve management efficiency.
- **Story 3.** I want borrowers to be able to view costume care instructions themselves so that it reduces repetitive work and extends the lifespan of the costumes.
- **Story 4.** I would like the system to automatically send expiration reminder emails to borrowers, thereby reducing overdue instances and improving the turnover rate of costumes.

#### As a Legislator

- **Story 1:** I want student data to be securely stored so that data protection and privacy laws are obeyed.

## Basic Flow

#### For a Booker:

**1.** Browse & search the costume catalogue.

**2a.** View details of a selected costume.

**2b.** If the costume has no image, submit an image upload request.

**3.** Select rental dates.

**4.** Click **`Book`** and log in if required.

**5.** Submit the request.

**6.** Receive the confirmation.

#### For an Admin:

**1.** Log in to the admin dashboard.

**2a.** Add a new costume to the catalogue.

**2b.** Select a costume and view its loan history.

**2c.** View and approve / reject image upload requests.

## Timeline

### MVP

| **Feature**     | **Progress**                | **Future Improvements**             |
| --------------- | --------------------------- | ----------------------------------- |
| Home page       | Full functionality          | Background images to look nicer     |
| Navbar          | Full functionality          | Mobile compatible                   |
| Catalogue       | Full functionality          | Nicer UX for Pagination             |
| Filters         | Full functionality          | Adding UK size guides               |
| Costume details | Full functionality          | Nicer text printing                 |
| Calendar        | Full functionality          | Fix TS error                        |
| Booking         | Frontend functionality      | Backend functionality, login prompt |
| CI              | Tests written               | Add to GitHub workflows             |
| CD              | Dockerfile & workflow setup | Debugging required                  |

### Beta

| **Feature**            | **Progress**          | **Future Improvements**                         |
| ---------------------- | --------------------- | ----------------------------------------------- |
| CI                     | High code coverage    | Test-driven development                         |
| CD                     | Full functionality    | Optimisation e.g. not a new link every new time |
| Booking                | Full functionality    | Integrate with user accounts                    |
| Logins                 | Full functionality    | Add middleware                                  |
| Admin dashboard        | Full functionality    | -                                               |
| User dashboard         | In progress           | -                                               |
| Uploading images       | Full functionality    | -                                               |
| Uploading new costumes | Full functionality    | Admin approval of user-suggested uploads        |
| AI suggested filters   | Todo                  | -                                               |

## Naming Guidelines

#### \* New Branch

```
<type>/<short-description>

feature/  →   New feature                                             [e.g., feature/navbar-update]
fix/      →   Bug fix or functional issue resolution                  [e.g., fix/costumelist-text-truncation]
docs/     →   Small but urgent documentation updates                  [e.g., docs/readme-naming-guidelines]
test/     →   Add unit or integration tests                           [e.g., test/booking-flow-test]
chore/    →   Maintenance tasks, improve CI/CD, Dockerfile updates    [e.g., chore/Docker]
```

> [!TIP]
> - Use lowercase letters with hyphens (`-`) to separate words
> - Ensure branch name matches PR title closely for easier tracking
> - Note that the `documentation` branch is reserved for text-only changes and will be merged during a release
    - The `docs/` naming is to avoid naming conflicts with the `documentation` branch

#### \* Pull Request

```
Type: Short description

Examples:
Feature: Add Costume Upload Endpoint
Fix: Correct Costume Availability Label Display
Docs: Update README with Naming Guidelines
Test: Add Integration Tests for Booking Flow
Chore: Update Dockerfile and CI/CD Configuration
```

> [!TIP]
> - Keep the title short, clear, and in imperative mood
> - Avoid dates or numbers in PR titles unless necessary

## Team Members

### 会议（线下 + 线上）
线下利用课后时间...
