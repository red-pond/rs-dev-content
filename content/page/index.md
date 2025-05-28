---
title: Home
description: "Riverscapes Developer Resources"
banner: true
isHome: false
---

import { Container } from '@mui/material'
import CardImage from '/static/images/card-image.jpg'

<Container maxWidth="xl">

Welcome to the Riverscapes Developer Portal, your go-to resource for developers and advanced users within the  [Riverscapes Consortium](https://riverscapes.net). Explore our [standards](./standards/), harness our [APIs](./api/), and ensure your models, code, and data adhere to our standards so they can be badged "Riverscapes-Compliant". Discover how our tools are crafted, learn about the data they generate, and find out how you can contribute your own tools and models.

## Resources for Developers

<Container maxWidth="xl">
    <Grid container spacing={4} sx={{mt: 3}} padding={0}>
      <StoryCard 
        title="Standards & Compliance"
        image={CardImage}
        description="Learn about riverscapes standards and how to make your tools and data compliant."
        to="/standards" />
      <StoryCard 
        title="Riverscapes API"
        image={CardImage}
        description="Learn how to use the Riverscapes API to access data."
        to="/getting-started" />
      <StoryCard 
        title="Documentation"
        image={CardImage}
        description="Resources to build Riverscapes documentation and websites."
        to="/documentation" />
    </Grid>
</Container>

## Other Riverscapes Sites

<Container maxWidth="xl">
    <Grid container spacing={4} sx={{mt: 3}} padding={0}>
      <StoryCard 
        title="Riverscapes Consortium"
        image={CardImage}
        description="The Riverscapes Consortium main site."
        to="https://riverscapes.net" />
      <StoryCard 
        title="Our Tools"
        image={CardImage}
        description="Learn about each of our Riverscapes compliant tools."
        to="https://tools.riverscapes.net" />
      <StoryCard 
        title="Data Exchange"
        image={CardImage}
        description="Discover and download Riverscapes compliant data."
        to="https://data.riverscapes.net" />
    </Grid>
</Container>

</Container>