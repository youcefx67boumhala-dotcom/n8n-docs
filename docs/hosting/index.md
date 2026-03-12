{ "workflow_name": "Youssef Funny Monkey Bot", "description": "روبوت تلقائي لصناعة فيديوهات قرد كرتوني مضحك ونشرها على YouTube بعد موافقة المستخدم.", "nodes": [ { "name": "Daily Schedule Trigger", "type": "Schedule", "config": { "times_per_day": 6 } }, { "name": "Trend Analysis", "type": "AI_Trend_Search", "config": { "keywords": ["funny monkey", "cartoon", "viral"] } }, { "name": "Script Generation", "type": "AI_Text_Generator", "config": { "prompt": "Create a 20-30 second funny cartoon monkey story for YouTube Shorts in English." } }, { "name": "Video Generation", "type": "AI_Video_Generator", "config": { "style": "Cartoon Monkey", "duration_seconds": 20, "resolution": "4K", "aspect_ratio": "9:16" } }, { "name": "Title & Hashtags Generator", "type": "AI_Text_Generator", "config": { "prompt": "Generate title and hashtags for a funny cartoon monkey short video." } }, { "name": "Manual Approval", "type": "Approval_Node", "config": { "send_to_user": "Youssef", "options": ["Publish", "Reject"] } }, { "name": "Upload to YouTube", "type": "YouTube_Upload", "config": { "channel_email": "youceffunnymonkey@gmail.com", "upload_after_approval": true } }, { "name": "Analytics & Learning", "type": "Analytics_Node", "config": { "track": ["views", "watch_time", "engagement"], "adjust_future_videos": true } } ] }---
title: n8n Hosting Documentation and Guides
description: Access n8n hosting documentation and guides. Find comprehensive resources to help you set up and manage your self-hosted n8n instances.
contentType: overview
hide:
  - toc
  - feedback
  - kapaButton
---

# Self-hosting n8n

This section provides guidance on setting up n8n for both the Enterprise and Community self-hosted editions. The Community edition is free, the Enterprise edition isn't. 

See [Community edition features](/hosting/community-edition-features.md) for a list of available features. 

<div class="grid-cards-vertical cards" markdown>

- __Installation and server setups__

	Install n8n on any platform using npm or Docker. Or follow our guides to popular hosting platforms.

	[:octicons-arrow-right-24: Docker installation guide](/hosting/installation/docker.md)

- __Configuration__

	Learn how to configure n8n with environment variables.

	[:octicons-arrow-right-24: Environment Variables](/hosting/configuration/environment-variables/index.md)

- __Users and authentication__

	Choose and set up user authentication for your n8n instance.

	[:octicons-arrow-right-24: Authentication](/hosting/configuration/user-management-self-hosted.md)

- __Scaling__

	Manage data, modes, and processes to keep n8n running smoothly at scale.

	[:octicons-arrow-right-24: Scaling](/hosting/scaling/queue-mode.md)

- __Securing n8n__

	Secure your n8n instance by setting up SSL, SSO, or 2FA or blocking or opting out of some data collection or features.

	[:octicons-arrow-right-24: Securing n8n guide](/hosting/securing/overview.md)

- __Starter kits__

	New to n8n or AI? Try our Self-hosted AI Starter Kit. Curated by n8n, it combines the self-hosted n8n platform with compatible AI products and components to get you started building self-hosted AI workflows.

	[:octicons-arrow-right-24: Starter kits](/hosting/starter-kits/ai-starter-kit.md)

</div>

--8<-- "_snippets/self-hosting/warning.md"
