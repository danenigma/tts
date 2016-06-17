#!/usr/bin/env python
#-*- coding:utf-8 -*-
import espeak
import rospy
from std_msgs.msg import String
class Tts():
	NODE_NAME = 'tts'
	def __init__(self):
		rospy.init_node(self.NODE_NAME)
		self.sub = rospy.Subscriber('/tts_text',String,self.tts_callback)
		self.es  = espeak.ESpeak()		
	def tts_callback(self,text):
		self.es.say(text.data)

if __name__ == "__main__":
	t = Tts()
	try:
		rospy.spin()
	except:
		print "Error!"
			
