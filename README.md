## Introduction

This readme will provide a description of how I completed this coding challenge to the best of my abilities.

## Reading the data

I used pandas to read the csv file of the traffic light data. I used numpy to read the .npz point cloud files. I experimented to figure out the format of the point clouds.

## Tracking the traffic light

I created a function to find the center of a bounding box. I then applied the function to each bounding box in the dataframe to find the center of the traffic light in each frame. Finally, I used the point cloud files to create a list of coordinates for the light. 

## Tracking the golf cart

I used a png viewer to find a source pixel on the golf cart in the first frame. I found the distance from that point and played with bounding boxes and thresholds in multiples of distances from the source pixel and found best possible mask for the golf cart. I then found the medioid pixel for the mask and the average (x, y, z) distance of all the pixels and used the medioid pixel as the source pixel for the next frame. 

## Visualizing the data

I reversed the traffic light data to make it the distance from the light to the car instead of to the light from the car. I then added the distances from the light to the car and the car to the golf cart to get the distance from the light to the golf cart. I then plotted each data point for both the golf cart and the ego car at the rate of 30 points per second to create the video.
