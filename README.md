# The SVO-Probes Dataset for Verb Understanding

This repository contains the SVO-Probes benchmark designed to probe for
*S*ubject, *V*erb, and *O*bject understanding in image--language models. This
benchmark provides two positive and negative images for a given sentence. The
negative image differs from the positive one with respect to either subject,
verb, or object. Given a sentence, we test if a model can correctly classify
both positive and negative images.

For a detailed description of our benchmark, please see the paper [Probing
Image–Language Transformers for Verb
Understanding](https://arxiv.org/abs/2106.09141).  Please cite this paper if
you use the SVO-Probes benchmark in your work.

### Files
* svo_probes.csv: our raw data. Each row in the dataset consists of two
  <sentence,positive-image> and <sentence,negative-image> pairs. Each image is
  identified by a url and a unique id: pos_image_id (pos_url) or neg_image_id
  (neg_url) to mark the positive and negative images, respectively. Each image
  is also associated with subject-verb-object triplets (pos_triplet or
  neg_triplet) that can be seen in the image. The subj_neg, verb_neg, obj_neg
  columns specify the type of the negative: for example, subj_neg is True if the
  negative example is a subject negative.

* image_urls.txt: a list of image urls used in our benchmark.

* A Colab to analyze pre-trained models on SVO-Probes.

## Disclaimer

This is not an official Google product. The SVO-Probes benchmark is created
solely for research purposes and is not intended to be used in products. The
images in our benchmark are retrieved from the Google Image Search; we expect
our images to reflect distributional properties and biases similar to those
returned by the Google Image Search API.  Furthermore, our dataset is designed
to have a similar vocabulary to the
Conceptual Captions dataset so we expect our <Subject, Verb, Object> triplets to
reflect biases in the Conceptual Captions.

## License
The data is made available under the terms of the Creative Commons Attribution
4.0 International Public License (CC BY 4.0). You can find details at:
https://creativecommons.org/licenses/by/4.0/legalcode")


If you have concerns or comments about the benchmark, please contact lmh@deepmind.com
and nematzadeh@deepmind.com.



