---
layout: post
title: Save Changes to a Note
date: 2018-01-30 00:00:00
description: For a user to be able to edit a note in our React.js app, we need to make a PUT request to our severless backend API using AWS Amplify. We also need to allow them to upload files directly to S3 and add that as an attachment to the note.
context: frontend
comments_id: 55
---

Now that our note loads into our form, let's work on saving the changes we make to that note.

<img class="code-marker" src="{{ site.baseurl }}/assets/s.png" />Replace the `handleSubmit` method in `src/containers/Notes.js` with the following.

``` coffee
saveNote(note) {
  return API.put("notes", `/notes/${this.props.match.params.id}`, {
    body: note
  });
}

handleSubmit = async event => {
  let attachment;

  event.preventDefault();

  if (this.file && this.file.size > config.MAX_ATTACHMENT_SIZE) {
    alert("Please pick a file smaller than 5MB");
    return;
  }

  this.setState({ isLoading: true });

  try {
    if (this.file) {
      attachment = await s3Upload(this.file);
    }

    await this.saveNote({
      content: this.state.content,
      attachment: attachment || this.state.note.attachment
    });
    this.props.history.push("/");
  } catch (e) {
    alert(e);
    this.setState({ isLoading: false });
  }
}

```

<img class="code-marker" src="{{ site.baseurl }}/assets/s.png" />And include our `s3Upload` helper method in the header:

``` javascript
import { s3Upload } from "../libs/awsLib";
```

The code above is doing a couple of things that should be very similar to what we did in the `NewNote` container.

1. If there is a file to upload we call `s3Upload` to upload it and save the key we get from S3.

2. We save the note by making a `PUT` request with the note object to `/notes/:id` where we get the `id` from `this.props.match.params.id`. We use the `API.put()` method from AWS Amplify.

3. And on success we redirect the user to the homepage.

Let's switch over to our browser and give it a try by saving some changes.

![Notes page saving screenshot]({{ site.baseurl }}/assets/react/listing-page-saving.png)

You might have noticed that we are not deleting the old attachment when we upload a new one. To keep things simple, we are leaving that bit of detail up to you. It should be pretty straightforward. Check the [AWS Amplify API Docs](https://aws.github.io/aws-amplify/api/classes/storageclass.html#remove) on how to a delete file from S3.

Next up, let's allow users to delete their note.
