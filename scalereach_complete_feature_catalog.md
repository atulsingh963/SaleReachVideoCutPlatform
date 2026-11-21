# ScaleReach.ai — Complete Public Feature Catalog & Product Requirements Reference

**Research date:** 2026-11-17  
**Purpose:** Feature-level reference for designing an independently implemented AI long-video-to-short-video SaaS.  
**Companion document:** `scalereach_architecture_blueprint.md` (technical architecture and implementation).  

> **Evidence labels:** **[D] Documented** in the public help centre, pricing, website or API docs; **[M] Marketed** as a named tool/use case, but detailed controls have not been independently verified; **[R] Recommended** product requirement to build a complete competitor, **not** confirmed to exist in ScaleReach; **[U] Unverified** implementation detail. This catalog does **not** claim authenticated access to the private dashboard.

## 1. Product definition

ScaleReach publicly presents an AI video repurposing platform: import a long video, automatically identify clips, apply captions/reframing, edit and export clips, and schedule publication. It also markets specialized tools, multi-workspace/team functionality, an API, and MCP-based integrations.

**Primary personas:** individual creators, podcasters, streamers, educators, agencies managing multiple brands, and enterprise media teams. These are use-case interpretations, not confirmed customer segments.

**Core user journey:** Sign up → create workspace → import source video → choose clip settings → processing → review scored clips → edit → export/share → connect social account → schedule/publish → monitor outcome.

## 2. Video ingestion & project creation

| ID | Feature / ability | Evidence | Detailed product behavior / scope |
|---|---|---|---|
| ING-01 | Upload local video | D | Choose a file and start video-processing job. |
| ING-02 | Import YouTube URL | D | Paste URL and generate clips. |
| ING-03 | Import Twitch link | D | Publicly advertised supported source. |
| ING-04 | Import Kick link | D | Publicly advertised supported source. |
| ING-05 | Import Google Drive link | D | Publicly advertised supported source. |
| ING-06 | Import Dropbox link | D | Publicly advertised supported source. |
| ING-07 | Import Loom link | D | Publicly advertised supported source. |
| ING-08 | Import Rumble link | D | Publicly advertised supported source. |
| ING-09 | Import Dailymotion link | D | Publicly advertised supported source. |
| ING-10 | Import Wistia link | D | Publicly advertised supported source. |
| ING-11 | Import Vidyard link | D | Publicly advertised supported source. |
| ING-12 | Import Streamable link | D | Publicly advertised supported source. |
| ING-13 | Import direct video URL | D | URL-based source ingestion. |
| ING-14 | MP4 support | D | Pricing FAQ lists common video formats. |
| ING-15 | MOV support | D | Pricing FAQ lists common video formats. |
| ING-16 | AVI support | D | Pricing FAQ lists common video formats. |
| ING-17 | MKV support | D | Pricing FAQ lists common video formats. |
| ING-18 | WebM support | U | Not independently confirmed from current pricing excerpt. |
| ING-19 | Source video duration limits | D | Free up to 30 minutes; Pro up to 3 hours per pricing table. |
| ING-20 | Source upload size limits | D | Free up to 2 GB; Pro up to 4 GB in comparison table. |
| ING-21 | Aspect-ratio selection before processing | D | Getting-started help guide describes this step. |
| ING-22 | Caption-style selection before processing | D | Getting-started help guide describes this step. |
| ING-23 | Job status and processing stages | D | Four-stage processing guide; API status polling. |
| ING-24 | Upload validation and error messages | R | Check file type, size, duration, corruption, permissions, unsupported URL. |
| ING-25 | Cancel/retry processing | R | Explicit cancellation, safe retry, idempotency. |
| ING-26 | Multi-file batch import | U | Do not claim until authenticated testing. |

## 3. AI transcription and understanding

| ID | Feature / ability | Evidence | Detailed product behavior / scope |
|---|---|---|---|
| AI-01 | Automatic speech transcription | D | Source audio becomes searchable/usable text for clip discovery. |
| AI-02 | Word-by-word caption timing | D | Publicly marketed word-by-word captions. |
| AI-03 | AI viral moment discovery | D | Identify engaging transcript segments. |
| AI-04 | Detect opening hooks | D | Pricing FAQ describes viral hooks. |
| AI-05 | Detect emotional peaks | D | Pricing FAQ describes emotional peaks. |
| AI-06 | Detect key insights | D | Pricing FAQ describes key insights. |
| AI-07 | Generate multiple short clips | D | Main platform promise. |
| AI-08 | Virality score per clip | D | Help guide describes scores and interpretation. |
| AI-09 | Analyze hook strength separately | U | Potential scoring dimension; not confirmed as a separate UI metric. |
| AI-10 | Analyze pacing separately | U | Potential scoring dimension; not confirmed as a separate UI metric. |
| AI-11 | Explain scoring rationale | U | Score exists; detailed explainability UI not verified. |
| AI-12 | AI video summarizer | M | Named website tool; exact outputs and controls unverified. |
| AI-13 | AI hook generator | M | Named website tool; exact workflow unverified. |
| AI-14 | Language auto-detection | R | Useful for multilingual transcription. |
| AI-15 | Speaker diarization | R | Useful for podcasts/interviews; not verified. |
| AI-16 | Profanity filtering | R | Optional caption/content filter. |
| AI-17 | Custom clip length preferences | R | User-configurable min/max clip durations. |
| AI-18 | Topic/keyword-based clip search | R | Discover segments by topic, phrase, or audience. |
| AI-19 | Clip deduplication | R | Avoid near-identical outputs from overlapping moments. |
| AI-20 | Model confidence and review flags | R | Flag uncertain transcription or poor audio. |

## 4. Clip review, library and selection

| ID | Feature / ability | Evidence | Detailed product behavior / scope |
|---|---|---|---|
| LIB-01 | View generated clips for a source video | D | Review AI-selected results. |
| LIB-02 | See virality scores | D | Scores help rank/select candidates. |
| LIB-03 | Clip library across workspace videos | D | Help guide explicitly describes this. |
| LIB-04 | Filter clip library | D | Help guide explicitly mentions filters. |
| LIB-05 | Favorite clips | D | Help guide explicitly mentions favoriting. |
| LIB-06 | Download clips | D | Help and pricing mention downloads. |
| LIB-07 | Share clip without recipient account | D | Help centre describes external sharing. |
| LIB-08 | Clip previews | D | Review/edit workflow implies preview; exact UI controls unverified. |
| LIB-09 | Clip tags and folders | R | Organize many clips across campaigns. |
| LIB-10 | Bulk delete/archive | R | Library management for high volume. |
| LIB-11 | Compare candidates side by side | R | Compare duration, score, topic and framing. |
| LIB-12 | Search transcripts across library | R | Useful but not verified. |
| LIB-13 | Share-link expiration and permissions | R | Security and access control for public links. |
| LIB-14 | Clip view count on share page | U | Not confirmed in current public documentation. |

## 5. Video editor and creative controls

| ID | Feature / ability | Evidence | Detailed product behavior / scope |
|---|---|---|---|
| EDT-01 | Edit an AI-generated clip | D | Help centre has dedicated edit guide. |
| EDT-02 | Change clip start time | D | Edit guide explicitly mentions changing boundaries. |
| EDT-03 | Change clip end time | D | Edit guide explicitly mentions changing boundaries. |
| EDT-04 | Correct caption text | D | Edit guide explicitly mentions caption correction. |
| EDT-05 | Change framing | D | Edit guide explicitly mentions framing. |
| EDT-06 | AI reframe / auto-zoom | D | Pricing page lists AI Reframe. |
| EDT-07 | Change video layout | D | Edit guide describes layout controls. |
| EDT-08 | Add hook overlay | D | Edit guide mentions hooks. |
| EDT-09 | Add text overlay | D | Edit guide mentions text. |
| EDT-10 | Add image overlay | D | Edit guide mentions images. |
| EDT-11 | Split-screen layout | D | Pricing comparison lists split-screen on Pro. |
| EDT-12 | Aspect ratio 9:16 | D | Pricing comparison. |
| EDT-13 | Aspect ratio 16:9 | D | Pricing comparison. |
| EDT-14 | Aspect ratio 1:1 | D | Pricing comparison. |
| EDT-15 | AI video editor | M | Named website tool; specific advanced editing controls not fully audited. |
| EDT-16 | Headline match cut | M | Named website tool. |
| EDT-17 | Video silence remover | M | Named website tool. |
| EDT-18 | Video resizer | M | Named website tool. |
| EDT-19 | Video compressor | M | Named website tool. |
| EDT-20 | Custom clip timeline tracks | U | UI structure not independently verified. |
| EDT-21 | Undo/redo | R | Essential non-destructive editor behavior. |
| EDT-22 | Keyboard shortcuts | R | Editor usability. |
| EDT-23 | Save draft / autosave | R | Preserve editing progress. |
| EDT-24 | Multi-track audio | R | Music, voice and source-audio controls. |
| EDT-25 | Animated crop keyframes | R | Manual override for AI framing. |
| EDT-26 | B-roll and stock library | U | Not verified as ScaleReach feature. |
| EDT-27 | Brand logo/watermark overlay | R | Useful brand-kit integration; not confirmed as a standalone control. |

## 6. Captions and typography

| ID | Feature / ability | Evidence | Detailed product behavior / scope |
|---|---|---|---|
| CAP-01 | Auto captions | D | Main product capability. |
| CAP-02 | Word-by-word animated captions | D | Pricing explicitly lists. |
| CAP-03 | Caption style selection | D | Getting-started guide. |
| CAP-04 | Caption corrections | D | Editing help guide. |
| CAP-05 | Highlight text animation | M | Named website tool. |
| CAP-06 | Font selection | U | Likely caption-style control, not confirmed in retrieved help index. |
| CAP-07 | Font size adjustment | U | Not independently confirmed. |
| CAP-08 | Font color adjustment | U | Not independently confirmed. |
| CAP-09 | Caption position adjustment | U | Not independently confirmed. |
| CAP-10 | Caption animation presets | U | Word-by-word animation is documented; preset catalog not verified. |
| CAP-11 | Caption translation | U | Not verified as a public feature. |
| CAP-12 | Transcript download | M | Named website tool. |
| CAP-13 | Video transcription tool | M | Named website tool. |
| CAP-14 | Caption safe-zone guides | R | Avoid platform overlays. |
| CAP-15 | Custom caption style presets | R | Reusable design tokens per workspace. |
| CAP-16 | SRT/VTT export | U | Do not assume supported formats without testing. |

## 7. Render, export and download

| ID | Feature / ability | Evidence | Detailed product behavior / scope |
|---|---|---|---|
| EXP-01 | Export finished clips | D | Core product workflow. |
| EXP-02 | FHD / 1080p quality | D | Pricing comparison lists FHD and 1080p. |
| EXP-03 | 9:16 output | D | Pricing comparison. |
| EXP-04 | 16:9 output | D | Pricing comparison. |
| EXP-05 | 1:1 output | D | Pricing comparison. |
| EXP-06 | Watermark on Free | D | Pricing. |
| EXP-07 | No watermark on paid plans | D | Pricing. |
| EXP-08 | Batch export on Pro/Agency | D | Pricing. |
| EXP-09 | Unlimited downloads | D | Pricing comparison lists unlimited. |
| EXP-10 | Signed clip download URLs via API | D | API documentation. |
| EXP-11 | Select arbitrary resolution/format via API | D | API introduction advertises export in any format/resolution; actual endpoint details need validation. |
| EXP-12 | Download progress / retry | R | Resumable or retryable delivery. |
| EXP-13 | Render queue priorities | R | Fairness and paid-plan differentiation. |
| EXP-14 | Custom export presets | R | Per-platform bitrate, codec, audio loudness. |

## 8. Social accounts, scheduling and publishing

| ID | Feature / ability | Evidence | Detailed product behavior / scope |
|---|---|---|---|
| PUB-01 | Connect social accounts | D | Help centre publishing guide. |
| PUB-02 | TikTok publishing/scheduling | D | Help centre explicitly names TikTok. |
| PUB-03 | Instagram Reels publishing/scheduling | D | Help centre explicitly names Instagram Reels. |
| PUB-04 | YouTube Shorts publishing/scheduling | D | Help centre explicitly names Shorts. |
| PUB-05 | Social scheduling calendar | D | Help centre explicitly mentions calendar. |
| PUB-06 | Scheduled post status | D | Help centre mentions published/failed. |
| PUB-07 | Failed post visibility | D | Help centre mentions failures. |
| PUB-08 | Five social accounts on Pro | D | Pricing. |
| PUB-09 | Unlimited social accounts on Agency | D | Pricing. |
| PUB-10 | X/Twitter publishing | U | Not confirmed in retrieved help/pricing. |
| PUB-11 | LinkedIn publishing | U | Not confirmed in retrieved help/pricing. |
| PUB-12 | Caption/hashtag composer | R | Per-platform metadata before publishing. |
| PUB-13 | OAuth token refresh and reconnect | R | Reliable official API integration. |
| PUB-14 | Posting retry and error reason | R | Operationally important. |
| PUB-15 | Cross-platform post analytics | U | Not verified as built-in capability. |
| PUB-16 | Best-time-to-post recommendations | U | Not verified. |

## 9. Workspaces, brand kits and collaboration

| ID | Feature / ability | Evidence | Detailed product behavior / scope |
|---|---|---|---|
| WRK-01 | Create workspace | D | Getting-started help guide. |
| WRK-02 | Workspace videos and clips | D | Workspace description. |
| WRK-03 | Workspace brand kit | D | Workspace settings help. |
| WRK-04 | Workspace social accounts | D | Workspace description. |
| WRK-05 | Rename workspace | D | Workspace settings guide. |
| WRK-06 | Invite team members | D | Workspace settings guide. |
| WRK-07 | Team collaboration | D | Agency/Enterprise pricing. |
| WRK-08 | One workspace on Free | D | Pricing. |
| WRK-09 | Three workspaces on Pro | D | Pricing. |
| WRK-10 | Ten workspaces on Agency | D | Pricing. |
| WRK-11 | Ten team members on Agency | D | Pricing. |
| WRK-12 | Workspace-specific member access | D | Help guide discusses invited-member access. |
| WRK-13 | Granular custom roles | U | Not verified. |
| WRK-14 | Approval workflow | R | Agency review and client signoff. |
| WRK-15 | Brand kit colors/fonts/logos | U | Brand kit documented; exact fields not verified. |
| WRK-16 | Workspace audit log | R | Track sensitive actions. |

## 10. Accounts, security, plans and metering

| ID | Feature / ability | Evidence | Detailed product behavior / scope |
|---|---|---|---|
| ACC-01 | Registration and login | D | Public links to app signup/login. |
| ACC-02 | Profile settings | D | Account/security help. |
| ACC-03 | Password management | D | Account/security help. |
| ACC-04 | Two-factor authentication | D | Account/security help. |
| ACC-05 | Passkeys | D | Account/security help. |
| ACC-06 | Subscription plan management | D | Billing help. |
| ACC-07 | Upgrade/downgrade mid-cycle | D | Billing help. |
| ACC-08 | Billing invoices | D | Billing help. |
| ACC-09 | Payment method management | D | Billing help. |
| ACC-10 | Usage minute balance | D | Minutes help. |
| ACC-11 | Usage transaction history | D | Minutes help. |
| ACC-12 | Free 100 one-time minutes | D | Pricing. |
| ACC-13 | Pro 400 minutes/month equivalent | D | Pricing comparison; promotional offer shows 4,800/year. |
| ACC-14 | Agency 60,000 minutes/year promotional allocation | D | Pricing. |
| ACC-15 | Storage retention limits | D | Free 24 hours; Pro 6 months per comparison table. |
| ACC-16 | Plan-based editing restrictions | D | Pricing says limited Free, unlimited Pro. |
| ACC-17 | Usage enforcement across API/UI | R | Avoid bypasses and duplicate charges. |
| ACC-18 | Data export and deletion controls | R | Privacy/compliance requirements. |

## 11. API, integrations and agent interfaces

| ID | Feature / ability | Evidence | Detailed product behavior / scope |
|---|---|---|---|
| API-01 | Workspace API keys | D | Help centre and API docs. |
| API-02 | Bearer token authentication | D | Public API example. |
| API-03 | Revoke API keys | D | API-key help guide. |
| API-04 | Submit YouTube video programmatically | D | `POST /api/videos/youtube`. |
| API-05 | Poll video processing status | D | `GET /api/videos/:id/status`. |
| API-06 | Retrieve generated clips | D | `GET /api/videos/:id/clips`. |
| API-07 | Retrieve clip scores/transcripts | D | API intro says clips include scores/transcripts. |
| API-08 | Retrieve signed download URLs | D | API intro. |
| API-09 | Programmatic export | D | API introduction advertises it; endpoint-specific details need validation. |
| API-10 | MCP server | D | Website and API docs advertise MCP. |
| API-11 | Claude integration | D | API docs explicitly mention Claude. |
| API-12 | Cursor integration | D | API docs explicitly mention Cursor. |
| API-13 | n8n integration through MCP | D | API docs explicitly mention n8n. |
| API-14 | Other MCP-compatible tools | D | API docs market 14+ tool connections; exact supported clients may vary. |
| API-15 | API key last-used timestamp | U | Not independently verified in current source excerpt. |
| API-16 | Webhooks for job completion | U | Not verified. |
| API-17 | API rate limits and quotas | U | Not verified. |
| API-18 | SDKs for JS/Python | U | Not verified. |

## 12. Specialized tools and use-case landing pages

The following are **named tools** in ScaleReach's public website navigation. A named page does **not** prove each tool has a distinct backend engine or all implied controls.

| ID | Named offering | Evidence | Intended use |
|---|---|---|---|
| TOOL-01 | AI Clip Generator | M | General automated clipping. |
| TOOL-02 | YouTube Thumbnail Downloader | M | Retrieve YouTube thumbnail images. |
| TOOL-03 | YouTube to Shorts | M | Turn YouTube videos into shorts. |
| TOOL-04 | AI Captions | M | Automatic captions. |
| TOOL-05 | AI Reframe | M | Adapt source framing to target aspect ratio. |
| TOOL-06 | AI Video Editor | M | Edit video clips. |
| TOOL-07 | Virality Score | M | Rank clip potential. |
| TOOL-08 | Subway Surfers Video Generator | M | Gaming-background style short clips. |
| TOOL-09 | Minecraft Video Generator | M | Minecraft-background style short clips. |
| TOOL-10 | ASMR Video Generator | M | ASMR-style video workflow. |
| TOOL-11 | Podcast to TikTok | M | Repurpose podcasts for TikTok. |
| TOOL-12 | Podcast to Reels | M | Repurpose podcasts for Instagram. |
| TOOL-13 | Twitch to TikTok | M | Repurpose stream highlights. |
| TOOL-14 | Webinar to Shorts | M | Repurpose webinars. |
| TOOL-15 | Video Transcription | M | Convert speech to text. |
| TOOL-16 | Download Transcript | M | Export video transcript. |
| TOOL-17 | AI Video Summarizer | M | Summarize video content. |
| TOOL-18 | Post Scheduler | M | Schedule social content. |
| TOOL-19 | AI Hook Generator | M | Suggest engaging intros. |
| TOOL-20 | Headline Match Cut | M | Named headline-editing workflow. |
| TOOL-21 | Highlight Text Animation | M | Emphasize words visually. |
| TOOL-22 | Video Silence Remover | M | Remove silent passages. |
| TOOL-23 | Video Resizer | M | Change dimensions/aspect ratio. |
| TOOL-24 | Video Compressor | M | Reduce video file size. |
| TOOL-25 | Gaming Highlight Clipper | M | Extract gaming highlights. |
| TOOL-26 | Interview to Clips | M | Extract interview excerpts. |
| TOOL-27 | Podcast Clip Maker | M | Extract podcast excerpts. |
| TOOL-28 | Talking Head Video Editor | M | Talking-head editing. |
| TOOL-29 | Tutorial Clip Generator | M | Extract instructional clips. |
| TOOL-30 | Video Highlight Generator | M | General highlight extraction. |

**Advertised industry/use-case categories:** YouTube, Podcast, TikTok, Instagram, Education, Fitness, Gaming, Coaching, Entertainment, Media, Streaming, News, Sports, Lifestyle, Marketing, Live Streaming. These are positioning categories, not necessarily separate features.

**Public site languages:** English, Spanish, Portuguese, French, German, Italian, Japanese, Chinese, Korean and Arabic are visible in the navigation. This establishes website localization, **not** automatic caption translation support.

## 13. Enterprise and support

| ID | Feature / ability | Evidence | Detailed product behavior / scope |
|---|---|---|---|
| ENT-01 | White-label solution | D | Enterprise plan offering. |
| ENT-02 | Custom AI training | D | Enterprise plan offering; technical scope undisclosed. |
| ENT-03 | Custom integrations | D | Enterprise plan offering. |
| ENT-04 | Dedicated account manager | D | Enterprise plan offering. |
| ENT-05 | SLA guarantee | D | Enterprise plan offering; terms undisclosed. |
| ENT-06 | Unlimited video uploads | D | Enterprise plan offering; subject to contract. |
| ENT-07 | Unlimited clip generation | D | Enterprise plan offering; subject to contract. |
| ENT-08 | Custom video length limits | D | Enterprise plan offering. |
| ENT-09 | Priority support | D | Agency pricing. |
| ENT-10 | Founder personal support | D | Pro/Agency pricing. |

## 14. Commercial feature matrix (public pricing snapshot)

| Capability | Free | Pro | Agency | Enterprise |
|---|---|---|---|---|
| Price displayed 2026-11-17 | $0 | Promotional $99/year | Promotional $348/year | Contact sales |
| Minutes | 100 one-time | 4,800/year promotion; 400/month comparison | 60,000/year promotion | Custom |
| Video length | Up to 30m | Up to 3h | Not separately specified in excerpt | Custom |
| Upload size | Up to 2GB | Up to 4GB | Not separately specified | Custom |
| Watermark | Yes | No | No | Contract |
| Storage retention | 24h | 6 months | Not separately specified | Contract |
| Workspaces | 1 | 3 | 10 | Custom |
| Social accounts | Not included | 5 | Unlimited | Custom |
| Team members | Not specified | Not specified | 10 | Custom |
| AI clip detection | Yes | Yes | Yes | Yes |
| AI reframe | Pricing sections inconsistent: Free card says yes, comparison says no | Yes | Not separately specified | Custom |
| Virality score | Yes | Yes | Yes/plan description | Custom |
| Split screen | No | Yes | Not separately specified | Custom |
| Social scheduling | No | Yes | Agency positioning suggests yes; verify checkout | Custom |
| Batch export | Not listed | Yes | Yes | Custom |

**Caution:** Prices are a time-limited promotion. Marketing sections can contradict comparison tables. Verify checkout and current plan entitlements before treating limits as contractual.

## 15. Suggested MVP parity checklist for your own product

These are **recommendations**, not extra ScaleReach claims.

### P0 — working AI clipping product
- [ ] Account + workspace creation
- [ ] Upload local file and import authorized YouTube URL
- [ ] Validate file type/size/duration
- [ ] Queue source processing and expose progress
- [ ] Generate transcript with word timestamps
- [ ] Identify semantically complete clip candidates
- [ ] Assign heuristic/LLM ranking score with honest uncertainty
- [ ] Render 9:16 clips with word-synced captions
- [ ] Review candidates in a library
- [ ] Edit clip boundaries and caption text
- [ ] Export MP4 and download
- [ ] Meter processing minutes safely
- [ ] Handle failed jobs, retries and duplicate submissions

### P1 — competitive creator editor
- [ ] AI reframing with face/speaker tracking
- [ ] Multiple caption templates and brand presets
- [ ] Text/image/hook overlays
- [ ] Split-screen layout
- [ ] 1:1 and 16:9 exports
- [ ] Batch export
- [ ] Share links with access controls
- [ ] Search/filter/favorite clips
- [ ] Clip editing autosave and undo/redo

### P2 — distribution and agencies
- [ ] OAuth connections for approved social platforms
- [ ] Schedule and publish with reliable retry
- [ ] Publishing calendar and failure states
- [ ] Workspace membership and roles
- [ ] Workspace brand kit
- [ ] Usage and billing dashboard
- [ ] Plan entitlements and subscription changes

### P3 — developer platform and enterprise
- [ ] API keys and scoped permissions
- [ ] Submit/poll/list/export API
- [ ] Webhooks and idempotency keys
- [ ] MCP server for agent-driven workflows
- [ ] Team audit logs
- [ ] White-label tenant configuration
- [ ] SLA monitoring and high-volume processing

## 16. Acceptance criteria examples for implementation

**Video import:** Given a supported file/URL and available quota, create a source video and processing job, show its state, and return either generated clips or an actionable error. Never silently double-charge on retry.

**AI clips:** For a source with speech, produce candidates with `start_ms`, `end_ms`, `transcript`, `score`, `score_version`, and a reviewable reason. Enforce source duration bounds and reject overlapping duplicate outputs as configured.

**Captions:** Every rendered word corresponds to an editable text token and timestamp; correcting a word does not require retranscribing the entire source.

**Editor:** Editing trim, captions, overlays or crop updates a non-destructive project revision; preview and final export should match within documented rendering tolerances.

**Publishing:** Every scheduled post has target account, platform, scheduled time zone, payload, status, attempt history and provider response; a retry must not create duplicate posts when provider confirmation is ambiguous.

**API:** API keys are scoped to workspace; unauthorized cross-workspace reads return no data; rate limiting and audit logging apply consistently.

## 17. Unknowns requiring hands-on competitor validation

1. Exact clip scoring formula, calibration and per-factor explanations.
2. Caption template catalog, fonts, animations and export formats.
3. Exact editor controls, timeline, transitions, undo/redo and autosave.
4. Real-time processing speeds and GPU/model architecture.
5. Which video URL integrations use OAuth versus public URLs.
6. Social platforms beyond TikTok, Instagram and YouTube.
7. Whether video summarization, ASMR and gaming generators are distinct functional products.
8. Supported transcript download formats and translation languages.
9. Whether public share links have expiration, analytics or embeds.
10. API rate limits, webhooks, bulk operations and SDK availability.
11. Agency plan upload-size, storage and video-length limits.
12. Detailed enterprise SLA, custom AI training, security and compliance commitments.

## 18. Public sources

- Main website and named tools: https://www.scalereach.ai/
- Pricing and plan comparison: https://www.scalereach.ai/pricing/
- Help centre and documented workflows: https://www.scalereach.ai/help/
- Clip editor: https://www.scalereach.ai/help/edit-a-clip/
- Processing stages: https://www.scalereach.ai/help/what-happens-during-processing/
- API documentation: https://docs.scalereach.ai/docs

**Research standard:** This document distinguishes advertised product functionality from implementation recommendations and unknowns. It is a competitor feature reference, not a reverse-engineered private specification. Build original UX, branding and code, and respect platform authorization and copyright requirements when importing content.
